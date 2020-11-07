---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 8AAD9309-5763-4903-AF6A-1E50310146C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 4b15f20f9399df277fc2d2a76f7e51c2a7d57d84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651305"
---
# <span data-ttu-id="66a2c-101">Set-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="66a2c-101">Set-AzDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="66a2c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66a2c-102">SYNOPSIS</span></span>
<span data-ttu-id="66a2c-103">Legt die Richtlinie für das automatische Herunterfahren einer Lab DevTest Labs fest.</span><span class="sxs-lookup"><span data-stu-id="66a2c-103">Sets the auto shutdown policy of a lab DevTest Labs.</span></span>

## <span data-ttu-id="66a2c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66a2c-104">SYNTAX</span></span>

### <span data-ttu-id="66a2c-105">Aktivieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="66a2c-105">Enable (Default)</span></span>
```
Set-AzDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66a2c-106">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="66a2c-106">Disable</span></span>
```
Set-AzDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66a2c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66a2c-107">DESCRIPTION</span></span>
<span data-ttu-id="66a2c-108">Das Cmdlet " **Set-AzDtlAutoShutdownPolicy** " legt die Richtlinie für das automatische Herunterfahren einer Übungseinheit fest, die alle virtuellen Computer in der Übungseinheit zu einer bestimmten Tageszeit automatisch herunterfährt.</span><span class="sxs-lookup"><span data-stu-id="66a2c-108">The **Set-AzDtlAutoShutdownPolicy** cmdlet sets the auto shutdown policy of a lab, which automatically shuts down all the virtual machines in the lab at a specified time of the day.</span></span>
<span data-ttu-id="66a2c-109">Das Cmdlet verwendet die angegebene Ressourcengruppe und den Namen der Übungseinheit, um die Richtlinie festzulegen.</span><span class="sxs-lookup"><span data-stu-id="66a2c-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="66a2c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66a2c-110">EXAMPLES</span></span>

## <span data-ttu-id="66a2c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="66a2c-111">PARAMETERS</span></span>

### <span data-ttu-id="66a2c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a2c-112">-DefaultProfile</span></span>
<span data-ttu-id="66a2c-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="66a2c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a2c-114">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="66a2c-114">-Disable</span></span>
<span data-ttu-id="66a2c-115">Gibt an, dass das Cmdlet die Richtlinie in der Übungseinheit deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="66a2c-115">Indicates that the cmdlet disables the policy in the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a2c-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="66a2c-116">-Enable</span></span>
<span data-ttu-id="66a2c-117">Gibt an, dass das Cmdlet die Richtlinie in der Übungseinheit aktiviert.</span><span class="sxs-lookup"><span data-stu-id="66a2c-117">Indicates that the cmdlet enables the policy in the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a2c-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="66a2c-118">-LabName</span></span>
<span data-ttu-id="66a2c-119">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet die Richtlinie für das automatische Herunterfahren festlegt.</span><span class="sxs-lookup"><span data-stu-id="66a2c-119">Specifies the name of the lab for which this cmdlet sets the auto shutdown policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66a2c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66a2c-120">-ResourceGroupName</span></span>
<span data-ttu-id="66a2c-121">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="66a2c-121">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66a2c-122">-Zeit</span><span class="sxs-lookup"><span data-stu-id="66a2c-122">-Time</span></span>
<span data-ttu-id="66a2c-123">Gibt die Uhrzeit als **DateTime** -Objekt für den Zeitpunkt an, zu dem die virtuellen Computer in der Übungseinheit heruntergefahren werden müssen.</span><span class="sxs-lookup"><span data-stu-id="66a2c-123">Specifies the time, as a **DateTime** object, for when the virtual machines in the lab must shut down.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a2c-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="66a2c-124">-Confirm</span></span>
<span data-ttu-id="66a2c-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66a2c-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a2c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66a2c-126">-WhatIf</span></span>
<span data-ttu-id="66a2c-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66a2c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66a2c-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66a2c-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a2c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a2c-129">CommonParameters</span></span>
<span data-ttu-id="66a2c-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66a2c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a2c-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66a2c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a2c-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66a2c-132">INPUTS</span></span>

### <span data-ttu-id="66a2c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="66a2c-133">System.String</span></span>

## <span data-ttu-id="66a2c-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66a2c-134">OUTPUTS</span></span>

### <span data-ttu-id="66a2c-135">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="66a2c-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="66a2c-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="66a2c-136">NOTES</span></span>

## <span data-ttu-id="66a2c-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66a2c-137">RELATED LINKS</span></span>

[<span data-ttu-id="66a2c-138">Get-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="66a2c-138">Get-AzDtlAutoShutdownPolicy</span></span>](./Get-AzDtlAutoShutdownPolicy.md)


