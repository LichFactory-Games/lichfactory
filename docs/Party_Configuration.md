`=round(([[Party Configuration]].TravelDistance * ([[Party Configuration]].varMins/(([[Party Configuration]].BaseSpeed / choice([[Party Configuration]].ExhaustionLevel > 1, 2, 1) + choice(contains([[Party Configuration]].Encumbered, true), -10, 0) + choice(contains([[Party Configuration]].HorseshoesofSpeed, true), 30, 0) + [[Party Configuration]].AdditionalBonus) / 10) * [[Party Configuration]].SpeedMultiplier)) / 60 / [[Party Configuration]].HoursPerDay, 1)`