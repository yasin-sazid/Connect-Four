# Connect Four — JavaFX Game with a Minimax Opponent

A desktop implementation of Connect Four combining an interactive JavaFX board with an adversarial search opponent. Developed as an academic group project, it demonstrates how game rules, heuristic evaluation, and a graphical interface work together in a playable AI application.

## Gameplay

- Play against the computer on a six-row, seven-column board.
- Choose a disc color and follow the turn indicator.
- Drop discs into available columns and watch the board update.
- Receive win and draw feedback, with in-application help and project information.

## AI design

The opponent searches up to **five plies** using minimax with **alpha–beta pruning**. Legal moves are generated from columns with available cells. Terminal states are scored with depth-sensitive utilities, while nonterminal positions use a board evaluation over potential four-disc winning patterns.

Immediate tactical checks identify opportunities to win or block the human player's next winning move. The evaluation favors unopposed patterns and combines their scores into an estimate of the position's value.

## Architecture

| Component | Responsibility |
| --- | --- |
| `src/sample/Main.java` | Board state, JavaFX controls, disc placement, and game lifecycle |
| `src/miniMaxPackage/Minimax.java` | Move generation, search, pruning, and tactical checks |
| `src/miniMaxPackage/EvaluationFunction.java` | Heuristic board scoring |
| `src/images/` | Game imagery |

## Launch

Open the project in a Java IDE with a JDK and JavaFX configured. Mark `src/` as the source root, retain its image resources on the runtime classpath, and run `sample.Main`. For a modular JavaFX installation, include the JavaFX controls and FXML modules in the launch configuration.

[The project report](AI_Connect_4_Report_1006_1015_1030.pdf) accompanies the implementation.

## Contributors

Yasin Sazid (BSSE 1006), Atkia Akila Karim (BSSE 1015), and Abdullah-Al-Jahid (BSSE 1030).
