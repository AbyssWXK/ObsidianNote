```mermaid
classDiagram
class GlySettingsActivity{
    -GlySettingsMenuAdapter mMenuAdapter
    -GlyFragmentAdapter mFragmentAdapter
}
class ViePagerAdapter{
-AssistFragment assistFragment
-LightFragment lightFragment
-SeatFragment seatFragment
-WindowFragment windowFragment
}
class AssistFragment
AssistFragment o-- ViePagerAdapter
class LightFragment
LightFragment o-- ViePagerAdapter
class SeatFragment
SeatFragment o-- ViePagerAdapter
class WindowFragment
WindowFragment o-- ViePagerAdapter
ViePagerAdapter o-- GlySettingsActivity
```