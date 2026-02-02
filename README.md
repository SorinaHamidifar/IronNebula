# ================================
# Project: FusionForge
# Description:
# A fusion of creativity and toughness—perfect for robust experiments,
# powerful prototypes, and evolving frameworks.
# ================================

# ---------- main.py ----------
"""
Main entry point for FusionForge.
"""

from core.creative import IdeaStudio
from core.framework import CoreFramework


def run():
    print("🔥 FusionForge Initialized")
    print("🎨 Creativity | 🛡️ Toughness | 🧩 Evolving Frameworks\n")

    studio = IdeaStudio()
    framework = CoreFramework()

    concepts = ["flow", "resilience", "velocity"]

    # Creative experimentation
    print("🎨 Concept Expansion:", studio.expand(concepts))

    # Prototype execution
    data = [4, 8, 16]
    print("⚙️ Prototype Output:", framework.execute(lambda x: x // 2, data))

    # Framework evolution
    print("📈 Framework Evolution:", framework.evolve({"stability": 0.9, "speed": 0.8}))


if __name__ == "__main__":
    run()


# ---------- core/creative.py ----------
"""
Creative experimentation and idea expansion module.
"""

class IdeaStudio:
    """Encourages creative transformations and exploratory logic."""

    def expand(self, ideas):
        """Expand ideas into richer conceptual forms."""
        return [f"{idea.upper()}_X" for idea in ideas]

    def remix(self, idea: str, intensity: int = 2) -> str:
        """Remix an idea multiple times."""
        return "-".join([idea] * intensity)


# ---------- core/framework.py ----------
"""
Durable core framework for robust and evolving systems.
"""

class CoreFramework:
    """Provides a tough, extensible backbone for prototypes and systems."""

    def execute(self, func, values):
        """Safely execute transformations."""
        try:
            return [func(v) for v in values]
        except Exception as e:
            return f"Execution failed: {e}"

    def evolve(self, metrics: dict, factor: float = 0.1) -> dict:
        """Evolve framework metrics gradually over time."""
        return {
            key: round(value * (1 + factor), 3)
            for key, value in metrics.items()
        }

    def integrity_check(self, metrics: dict) -> bool:
        """Ensure framework stability."""
        return all(0 <= v <= 1 for v in metrics.values())


# ---------- tests/test_framework.py ----------
"""
Tests for framework durability.
"""

from core.framework import CoreFramework

def test_execute():
    fw = CoreFramework()
    assert fw.execute(lambda x: x + 1, [1, 2]) == [2, 3]

def test_evolve():
    fw = CoreFramework()
    evolved = fw.evolve({"stability": 1.0})
    assert evolved["stability"] > 1.0

