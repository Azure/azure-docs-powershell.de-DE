---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 6c0b67bb70a364de45a88f80ca99bdec5e1d7188
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008230"
---
# <span data-ttu-id="9799f-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="9799f-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="9799f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9799f-102">SYNOPSIS</span></span>
<span data-ttu-id="9799f-103">Aktualisieren des intelligenten Gruppenstatus</span><span class="sxs-lookup"><span data-stu-id="9799f-103">Updates smart group state</span></span>

## <span data-ttu-id="9799f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9799f-104">SYNTAX</span></span>

### <span data-ttu-id="9799f-105">BySmartGroupId (Standard)</span><span class="sxs-lookup"><span data-stu-id="9799f-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9799f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9799f-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9799f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9799f-107">DESCRIPTION</span></span>
<span data-ttu-id="9799f-108">**Update-AzSmartGroupState-** Cmdlet aktualisiert den intelligenten Gruppen Zustand.</span><span class="sxs-lookup"><span data-stu-id="9799f-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="9799f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9799f-109">EXAMPLES</span></span>

### <span data-ttu-id="9799f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9799f-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="9799f-111">Mit diesem Cmdlet wird der Smart Group-Zustand auf angenommenen Auftrages sowie aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9799f-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="9799f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9799f-112">PARAMETERS</span></span>

### <span data-ttu-id="9799f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9799f-113">-DefaultProfile</span></span>
<span data-ttu-id="9799f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9799f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9799f-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9799f-115">-InputObject</span></span>
<span data-ttu-id="9799f-116">Eingabeobjekt aus Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9799f-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9799f-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="9799f-117">-SmartGroupId</span></span>
<span data-ttu-id="9799f-118">Eindeutiger Bezeichner der intelligenten Gruppe/Resourcen-ID der intelligenten Gruppe.</span><span class="sxs-lookup"><span data-stu-id="9799f-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9799f-119">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="9799f-119">-State</span></span>
<span data-ttu-id="9799f-120">Aktualisierter intelligenter Gruppenstatus</span><span class="sxs-lookup"><span data-stu-id="9799f-120">Updated Smart group State</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9799f-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9799f-121">-Confirm</span></span>
<span data-ttu-id="9799f-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9799f-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9799f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9799f-123">-WhatIf</span></span>
<span data-ttu-id="9799f-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9799f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9799f-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9799f-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9799f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9799f-126">CommonParameters</span></span>
<span data-ttu-id="9799f-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9799f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9799f-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9799f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9799f-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9799f-129">INPUTS</span></span>

### <span data-ttu-id="9799f-130">Keine</span><span class="sxs-lookup"><span data-stu-id="9799f-130">None</span></span>

## <span data-ttu-id="9799f-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9799f-131">OUTPUTS</span></span>

### <span data-ttu-id="9799f-132">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="9799f-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="9799f-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="9799f-133">NOTES</span></span>

## <span data-ttu-id="9799f-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9799f-134">RELATED LINKS</span></span>
