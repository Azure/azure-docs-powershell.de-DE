---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 8AAD9309-5763-4903-AF6A-1E50310146C0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: d812d66911c31297a2aaf4a32fd73562bc4ae9b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501881"
---
# <span data-ttu-id="a21d4-101">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="a21d4-101">Set-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="a21d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a21d4-102">SYNOPSIS</span></span>
<span data-ttu-id="a21d4-103">Legt die Richtlinie für das automatische Herunterfahren einer Lab DevTest Labs fest.</span><span class="sxs-lookup"><span data-stu-id="a21d4-103">Sets the auto shutdown policy of a lab DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a21d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a21d4-104">SYNTAX</span></span>

### <span data-ttu-id="a21d4-105">Aktivieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="a21d4-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a21d4-106">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="a21d4-106">Disable</span></span>
```
Set-AzureRmDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a21d4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a21d4-107">DESCRIPTION</span></span>
<span data-ttu-id="a21d4-108">Das Cmdlet " **Set-AzureRmDtlAutoShutdownPolicy** " legt die Richtlinie für das automatische Herunterfahren einer Übungseinheit fest, die alle virtuellen Computer in der Übungseinheit zu einer bestimmten Tageszeit automatisch herunterfährt.</span><span class="sxs-lookup"><span data-stu-id="a21d4-108">The **Set-AzureRmDtlAutoShutdownPolicy** cmdlet sets the auto shutdown policy of a lab, which automatically shuts down all the virtual machines in the lab at a specified time of the day.</span></span>
<span data-ttu-id="a21d4-109">Das Cmdlet verwendet die angegebene Ressourcengruppe und den Namen der Übungseinheit, um die Richtlinie festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a21d4-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="a21d4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a21d4-110">EXAMPLES</span></span>

## <span data-ttu-id="a21d4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a21d4-111">PARAMETERS</span></span>

### <span data-ttu-id="a21d4-112">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="a21d4-112">-Disable</span></span>
<span data-ttu-id="a21d4-113">Gibt an, dass das Cmdlet die Richtlinie in der Übungseinheit deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a21d4-113">Indicates that the cmdlet disables the policy in the lab.</span></span>

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

### <span data-ttu-id="a21d4-114">-Enable</span><span class="sxs-lookup"><span data-stu-id="a21d4-114">-Enable</span></span>
<span data-ttu-id="a21d4-115">Gibt an, dass das Cmdlet die Richtlinie in der Übungseinheit aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a21d4-115">Indicates that the cmdlet enables the policy in the lab.</span></span>

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

### <span data-ttu-id="a21d4-116">-LabName</span><span class="sxs-lookup"><span data-stu-id="a21d4-116">-LabName</span></span>
<span data-ttu-id="a21d4-117">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet die Richtlinie für das automatische Herunterfahren festlegt.</span><span class="sxs-lookup"><span data-stu-id="a21d4-117">Specifies the name of the lab for which this cmdlet sets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="a21d4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a21d4-118">-ResourceGroupName</span></span>
<span data-ttu-id="a21d4-119">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="a21d4-119">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="a21d4-120">-Zeit</span><span class="sxs-lookup"><span data-stu-id="a21d4-120">-Time</span></span>
<span data-ttu-id="a21d4-121">Gibt die Uhrzeit als **DateTime** -Objekt für den Zeitpunkt an, zu dem die virtuellen Computer in der Übungseinheit heruntergefahren werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a21d4-121">Specifies the time, as a **DateTime** object, for when the virtual machines in the lab must shut down.</span></span>

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

### <span data-ttu-id="a21d4-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a21d4-122">-Confirm</span></span>
<span data-ttu-id="a21d4-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a21d4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a21d4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a21d4-124">-WhatIf</span></span>
<span data-ttu-id="a21d4-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a21d4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a21d4-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a21d4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a21d4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a21d4-127">-DefaultProfile</span></span>
<span data-ttu-id="a21d4-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a21d4-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a21d4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a21d4-129">CommonParameters</span></span>
<span data-ttu-id="a21d4-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a21d4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a21d4-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a21d4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a21d4-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a21d4-132">INPUTS</span></span>

## <span data-ttu-id="a21d4-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a21d4-133">OUTPUTS</span></span>

### <span data-ttu-id="a21d4-134">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="a21d4-134">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="a21d4-135">Dieses Cmdlet gibt den Zeitplan zurück, der angibt, wann die virtuellen Computer in der Übungseinheit heruntergefahren werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a21d4-135">This cmdlet returns the schedule which specifies when the virtual machines in the lab must shut down.</span></span>

## <span data-ttu-id="a21d4-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="a21d4-136">NOTES</span></span>

## <span data-ttu-id="a21d4-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a21d4-137">RELATED LINKS</span></span>

[<span data-ttu-id="a21d4-138">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="a21d4-138">Get-AzureRmDtlAutoShutdownPolicy</span></span>](./Get-AzureRmDtlAutoShutdownPolicy.md)


