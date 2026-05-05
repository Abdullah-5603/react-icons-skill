# Icon Prefixes

Use this table to choose the right import path and icon family. Prefer the family already used by the surrounding UI before introducing a new one.

| Family | Import path | Prefix examples | Best for |
| --- | --- | --- | --- |
| Font Awesome 5 | `react-icons/fa` | `FaGithub`, `FaSearch` | classic UI/general icons |
| Font Awesome 6 | `react-icons/fa6` | `Fa6XTwitter` | newer Font Awesome icons |
| Feather | `react-icons/fi` | `FiSearch` | clean outline UI |
| Lucide | `react-icons/lu` | `LuSettings` | modern SaaS UI |
| Material Design | `react-icons/md` | `MdHome` | Material-style apps |
| Tabler | `react-icons/tb` | `TbHome` | dashboards |
| Heroicons | `react-icons/hi` | `HiHome` | Tailwind/Heroicons style |
| Heroicons 2 | `react-icons/hi2` | `HiMiniHome` | newer Heroicons |
| Remix Icon | `react-icons/ri` | `RiHomeLine` | product UI |
| Simple Icons | `react-icons/si` | `SiReact` | brand/logo icons |
| Bootstrap Icons | `react-icons/bs` | `BsBootstrap` | Bootstrap-style UI |
| Ant Design Icons | `react-icons/ai` | `AiOutlineHome` | Ant Design-style UI |
| Ionicons 5 | `react-icons/io5` | `IoHomeOutline` | mobile/app UI |
| Phosphor | `react-icons/pi` | `PiHouse` | flexible modern UI |
| Octicons | `react-icons/go` | `GoMarkGithub` | GitHub-style UI |

## Practical selection notes

- Use Simple Icons for brand logos when an exact brand match matters.
- Use Font Awesome when the project already uses classic `Fa` icons.
- Use Lucide, Tabler, or Feather for quiet product interfaces and dashboards.
- Use Material Design icons when the app already follows Material visual language.
- Avoid mixing outline, filled, and brand-heavy families in the same navigation area unless the design intentionally calls for it.
