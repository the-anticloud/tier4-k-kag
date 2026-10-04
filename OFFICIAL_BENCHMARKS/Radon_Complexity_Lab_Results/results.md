# Radon_Complexity_Lab_Results
**Project:** `K_KAG` | **Status:** `PASS` | **Run:** `2026-09-30T17:14:20.030944+00:00`

**Framework:** [Radon — Cyclomatic Complexity & Maintainability Index](https://radon.readthedocs.io/)

## Key Metrics

- **files_analyzed:** `10`
- **average_complexity:** `{'grade': 'A', 'score': 2.1538461538461537}`
- **complexity_grade:** `A`
- **complexity_score:** `2.1538461538461537`
- **mi_output:** `E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_KAG\UPSTREAM\setup.py - A (84.57)
E:\fenta\Downloads\The Anti`

## Raw Output (first 50 lines)
```
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_KAG\UPSTREAM\kag\_anticloud_egress.py
    F 38:0 _is_frontier - A (4)
    F 43:0 guarded_connect - A (4)
    F 61:0 install - A (3)
    F 33:0 is_offline - A (1)
    C 29:0 EgressDenied - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_KAG\UPSTREAM\kag\bin\base.py
    F 21:0 add_commands - A (4)
    C 37:0 Command - A (2)
    M 38:4 Command.get_handler - A (1)
    M 42:4 Command.add_to_parser - A (1)
    M 47:4 Command.handler - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_KAG\UPSTREAM\kag\bin\kag_cmds.py
    F 16:0 build_parser - A (1)
    F 34:0 main - A (1)
E:\fenta\Downloads\The Anticloud\TIER_4_INFERENCE_AGENTS\K_KAG\UPSTREAM\kag\bridge\spg_server_bridge.py
    M 93:4 SPGServerBridge.run_component - B (7)
    M 72:4 SPGServerBridge.run_reader - A (5)
    C 58:0 SPGServerBridge - A (3)
    M 62:4 SPGServerBridge.run_scanner - A (3)
    M 177:4 SPGServerBridge.get_index_manager_info - A (3)
    M 130:4 SPGServerBridge.run_builder - A (2)
    M 140:4 SPGServerBridge.run_solver - A (2)
    F 27:0 init_kag_config - A (1)
    F 33:0 collect_reader_outputs - A (1)
    M 59:4 SPGServerBridge.__init__ - A (1)
    M 118:4 SPGServerBridge.run_llm_config_check - A (1)
    M 123:4 SPGServerBridge.run_vectorizer_config_check - A (1)
    M 170:4 SPGServerBridge.get_llm_token_info - A (1)
    M 194:4 SPGServerBridge.get_index_manager_names - A (1)

26 blocks (classes, functions, methods) anal
```

---
_Anticloud Independent Benchmark — 2026-09-30T17:14:20.030944+00:00_