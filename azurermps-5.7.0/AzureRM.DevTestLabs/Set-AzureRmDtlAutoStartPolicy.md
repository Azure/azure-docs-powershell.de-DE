---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: 000c9f2748bd1f80559d9fc80c206e4f1c9bf0c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663490"
---
# <span data-ttu-id="70be2-101">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="70be2-101">Set-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="70be2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70be2-102">SYNOPSIS</span></span>
<span data-ttu-id="70be2-103">Legt die Richtlinie für den automatischen Start einer Übungseinheit in DevTest Labs fest.</span><span class="sxs-lookup"><span data-stu-id="70be2-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70be2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70be2-104">SYNTAX</span></span>

### <span data-ttu-id="70be2-105">Aktivieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="70be2-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70be2-106">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="70be2-106">Disable</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70be2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70be2-107">DESCRIPTION</span></span>
<span data-ttu-id="70be2-108">Das Cmdlet " **Set-AzureRmDtlAutoStartPolicy** " legt die Richtlinie für den automatischen Start einer Übungseinheit fest, mit der virtuelle Lab-Computer für den automatischen Start geplant werden können.</span><span class="sxs-lookup"><span data-stu-id="70be2-108">The **Set-AzureRmDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="70be2-109">Das Cmdlet verwendet die angegebene Ressourcengruppe und den Namen der Übungseinheit, um die Richtlinie festzulegen.</span><span class="sxs-lookup"><span data-stu-id="70be2-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="70be2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70be2-110">EXAMPLES</span></span>

## <span data-ttu-id="70be2-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="70be2-111">PARAMETERS</span></span>

### <span data-ttu-id="70be2-112">-Tage</span><span class="sxs-lookup"><span data-stu-id="70be2-112">-Days</span></span>
<span data-ttu-id="70be2-113">Gibt als Array die Wochentage an, zu denen die virtuellen Computer der Übungseinheit gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="70be2-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

```yaml
Type: DayOfWeek[]
Parameter Sets: (All)
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70be2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70be2-114">-DefaultProfile</span></span>
<span data-ttu-id="70be2-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="70be2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70be2-116">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="70be2-116">-Disable</span></span>
<span data-ttu-id="70be2-117">Gibt an, dass dieses Cmdlet die Richtlinie für die virtuellen Computer in der Übungseinheit deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="70be2-117">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70be2-118">-Enable</span><span class="sxs-lookup"><span data-stu-id="70be2-118">-Enable</span></span>
<span data-ttu-id="70be2-119">Gibt an, dass dieses Cmdlet die Richtlinie für die virtuellen Computer in der Übungseinheit aktiviert.</span><span class="sxs-lookup"><span data-stu-id="70be2-119">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70be2-120">-LabName</span><span class="sxs-lookup"><span data-stu-id="70be2-120">-LabName</span></span>
<span data-ttu-id="70be2-121">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet die Richtlinie für den automatischen Start festlegt.</span><span class="sxs-lookup"><span data-stu-id="70be2-121">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70be2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70be2-122">-ResourceGroupName</span></span>
<span data-ttu-id="70be2-123">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="70be2-123">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70be2-124">-Zeit</span><span class="sxs-lookup"><span data-stu-id="70be2-124">-Time</span></span>
<span data-ttu-id="70be2-125">Gibt den Zeitpunkt an, zu dem die virtuellen Computer der Übungseinheit gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="70be2-125">Specifies the time when the virtual machines of the lab must be started.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70be2-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="70be2-126">-Confirm</span></span>
<span data-ttu-id="70be2-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="70be2-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70be2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70be2-128">-WhatIf</span></span>
<span data-ttu-id="70be2-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70be2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70be2-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70be2-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70be2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70be2-131">CommonParameters</span></span>
<span data-ttu-id="70be2-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70be2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70be2-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70be2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70be2-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70be2-134">INPUTS</span></span>

### <span data-ttu-id="70be2-135">Keine</span><span class="sxs-lookup"><span data-stu-id="70be2-135">None</span></span>
<span data-ttu-id="70be2-136">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="70be2-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="70be2-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70be2-137">OUTPUTS</span></span>

### <span data-ttu-id="70be2-138">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="70be2-138">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="70be2-139">Dieses Cmdlet gibt den Zeitplan zurück, der angibt, wann die virtuellen Computer der Übungseinheit gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="70be2-139">This cmdlet returns the schedule that specifies when the virtual machines of the lab must be started.</span></span>

## <span data-ttu-id="70be2-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="70be2-140">NOTES</span></span>

## <span data-ttu-id="70be2-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70be2-141">RELATED LINKS</span></span>

[<span data-ttu-id="70be2-142">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="70be2-142">Get-AzureRmDtlAutoStartPolicy</span></span>](./Get-AzureRmDtlAutoStartPolicy.md)


