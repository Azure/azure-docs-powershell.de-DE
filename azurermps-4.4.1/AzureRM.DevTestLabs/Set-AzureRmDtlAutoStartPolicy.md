---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: a1efa9159bbe318a1de0360a3f70f197660db535
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663941"
---
# <span data-ttu-id="0880a-101">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="0880a-101">Set-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="0880a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0880a-102">SYNOPSIS</span></span>
<span data-ttu-id="0880a-103">Legt die Richtlinie für den automatischen Start einer Übungseinheit in DevTest Labs fest.</span><span class="sxs-lookup"><span data-stu-id="0880a-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0880a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0880a-104">SYNTAX</span></span>

### <span data-ttu-id="0880a-105">Aktivieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="0880a-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0880a-106">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="0880a-106">Disable</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0880a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0880a-107">DESCRIPTION</span></span>
<span data-ttu-id="0880a-108">Das Cmdlet " **Set-AzureRmDtlAutoStartPolicy** " legt die Richtlinie für den automatischen Start einer Übungseinheit fest, mit der virtuelle Lab-Computer für den automatischen Start geplant werden können.</span><span class="sxs-lookup"><span data-stu-id="0880a-108">The **Set-AzureRmDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="0880a-109">Das Cmdlet verwendet die angegebene Ressourcengruppe und den Namen der Übungseinheit, um die Richtlinie festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0880a-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="0880a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0880a-110">EXAMPLES</span></span>

## <span data-ttu-id="0880a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0880a-111">PARAMETERS</span></span>

### <span data-ttu-id="0880a-112">-Tage</span><span class="sxs-lookup"><span data-stu-id="0880a-112">-Days</span></span>
<span data-ttu-id="0880a-113">Gibt als Array die Wochentage an, zu denen die virtuellen Computer der Übungseinheit gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="0880a-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

```yaml
Type: System.DayOfWeek[]
Parameter Sets: (All)
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0880a-114">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="0880a-114">-Disable</span></span>
<span data-ttu-id="0880a-115">Gibt an, dass dieses Cmdlet die Richtlinie für die virtuellen Computer in der Übungseinheit deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0880a-115">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="0880a-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="0880a-116">-Enable</span></span>
<span data-ttu-id="0880a-117">Gibt an, dass dieses Cmdlet die Richtlinie für die virtuellen Computer in der Übungseinheit aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0880a-117">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="0880a-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="0880a-118">-LabName</span></span>
<span data-ttu-id="0880a-119">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet die Richtlinie für den automatischen Start festlegt.</span><span class="sxs-lookup"><span data-stu-id="0880a-119">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

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

### <span data-ttu-id="0880a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0880a-120">-ResourceGroupName</span></span>
<span data-ttu-id="0880a-121">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="0880a-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="0880a-122">-Zeit</span><span class="sxs-lookup"><span data-stu-id="0880a-122">-Time</span></span>
<span data-ttu-id="0880a-123">Gibt den Zeitpunkt an, zu dem die virtuellen Computer der Übungseinheit gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="0880a-123">Specifies the time when the virtual machines of the lab must be started.</span></span>

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

### <span data-ttu-id="0880a-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0880a-124">-Confirm</span></span>
<span data-ttu-id="0880a-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0880a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0880a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0880a-126">-WhatIf</span></span>
<span data-ttu-id="0880a-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0880a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0880a-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0880a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0880a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0880a-129">-DefaultProfile</span></span>
<span data-ttu-id="0880a-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0880a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0880a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0880a-131">CommonParameters</span></span>
<span data-ttu-id="0880a-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0880a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0880a-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0880a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0880a-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0880a-134">INPUTS</span></span>

## <span data-ttu-id="0880a-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0880a-135">OUTPUTS</span></span>

### <span data-ttu-id="0880a-136">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="0880a-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="0880a-137">Dieses Cmdlet gibt den Zeitplan zurück, der angibt, wann die virtuellen Computer der Übungseinheit gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="0880a-137">This cmdlet returns the schedule that specifies when the virtual machines of the lab must be started.</span></span>

## <span data-ttu-id="0880a-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="0880a-138">NOTES</span></span>

## <span data-ttu-id="0880a-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0880a-139">RELATED LINKS</span></span>

[<span data-ttu-id="0880a-140">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="0880a-140">Get-AzureRmDtlAutoStartPolicy</span></span>](./Get-AzureRmDtlAutoStartPolicy.md)


