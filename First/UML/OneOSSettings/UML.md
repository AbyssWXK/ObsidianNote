```mermaid
classDiagram
class GlyICarViewModel{
 IGlyCar mCar
 IGlyHev mHev
}
class GlyOneOSApiViewModel{
 NaviManager mNaviManager
 UserManager mUserManager
 DockBarManager mDockBarManager
 VrManager mVrManager
}
class GlySoundViewModel{
 IGlyAudio mGlyAudio
 Audio mAudio
}
class GlySystemViewModel{
 GlySystemInfo mGlySystem
}

class GlySettingsActivity{
    -GlySettingsMenuAdapter mMenuAdapter
    -GlyFragmentAdapter mFragmentAdapter
}
class ViePagerAdapter{
-GlyCarAssistantFragment fragment
-GlyCommonFragment fragment
-DriveAssistanceFragment fragment
-XXXFragment fragment
}
class GlyCarAssistantFragment{
 -GlyVehicleInfoDialog dialog
}
class GlyVehicleInfoDialog
GlyVehicleInfoDialog o-- GlyCarAssistantFragment
GlyCarAssistantFragment o-- ViePagerAdapter
class GlyCommonFragment
GlyCommonFragment o-- ViePagerAdapter
class DriveAssistanceFragment{
 -GlyDriveCMSFTipsDialog dialog 
 -GlyDriveCMSFWarnTipsDialog dialog 
 ...
}
class GlyDriveCMSFTipsDialog
GlyDriveCMSFTipsDialog *-- DriveAssistanceFragment
class GlyDriveCMSFWarnTipsDialog
GlyDriveCMSFWarnTipsDialog *-- DriveAssistanceFragment
DriveAssistanceFragment *-- ViePagerAdapter
class XXXFragment
XXXFragment *-- ViePagerAdapter
ViePagerAdapter *-- GlySettingsActivity

GlySettingsActivity ..> GlyOneOSApiViewModel
GlySettingsActivity ..> GlyICarViewModel
GlySettingsActivity ..> GlySoundViewModel
GlySettingsActivity ..> GlySystemViewModel

XXXFragment ..> GlyOneOSApiViewModel
XXXFragment ..> GlyICarViewModel
XXXFragment ..> GlySoundViewModel
XXXFragment ..> GlySystemViewModel



```
GlyCarAssistantFragment --> GlyBaseFragment
GlyCommonFragment --> GlyBaseFragment
DriveAssistanceFragment --> GlyBaseFragment
XXXFragment --> GlyBaseFragment


GlyCarAssistantFragment ..> GlyOneOSApiViewModel
GlyCarAssistantFragment ..> GlyICarViewModel
GlyCarAssistantFragment ..> GlySoundViewModel
GlyCarAssistantFragment ..> GlySystemViewModel

GlyCommonFragment ..> GlyOneOSApiViewModel
GlyCommonFragment ..> GlyICarViewModel
GlyCommonFragment ..> GlySoundViewModel
GlyCommonFragment ..> GlySystemViewModel

DriveAssistanceFragment ..> GlyOneOSApiViewModel
DriveAssistanceFragment ..> GlyICarViewModel
DriveAssistanceFragment ..> GlySoundViewModel
DriveAssistanceFragment ..> GlySystemViewModel

```mermaid
graph 

subgraph .
subgraph View
	Activity(Activity)
    Fragment(Fragment)
    Dialog(Dialog)
end
subgraph ViewModel
    GlyICarViewModel
    GlyOneOSApiViewModel
    GlySoundViewModel
    GlySystemViewModel
end
subgraph Model
    CarApi
    SystemApi
    OneOsApi
    SoundApi
end


end

```