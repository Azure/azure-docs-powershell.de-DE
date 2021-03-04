---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/remove-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 93c15d2675cc0e3e5fe0b37bc5af331ce97e7d8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919339"
---
# <span data-ttu-id="fa7c8-101">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="fa7c8-101">Remove-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="fa7c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa7c8-102">SYNOPSIS</span></span>
<span data-ttu-id="fa7c8-103">Löscht eine Instanz der eingebetteten PowerBI-Kapazität.</span><span class="sxs-lookup"><span data-stu-id="fa7c8-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="fa7c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa7c8-104">SYNTAX</span></span>

### <span data-ttu-id="fa7c8-105">ByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="fa7c8-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa7c8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fa7c8-106">ByResourceId</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa7c8-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fa7c8-107">ByInputObject</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa7c8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa7c8-108">DESCRIPTION</span></span>
<span data-ttu-id="fa7c8-109">Das Remove-AzPowerBIEmbeddedCapacity-Cmdlet löscht eine Instanz der eingebetteten PowerBI-Kapazität.</span><span class="sxs-lookup"><span data-stu-id="fa7c8-109">The Remove-AzPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="fa7c8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fa7c8-110">EXAMPLES</span></span>

### <span data-ttu-id="fa7c8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fa7c8-111">Example 1</span></span>
```
PS C:\> Remove-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="fa7c8-112">Mit diesem Befehl wird die Kapazität namens Testkapazität im RessourcengruppentestRG entfernt.</span><span class="sxs-lookup"><span data-stu-id="fa7c8-112">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="fa7c8-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fa7c8-113">PARAMETERS</span></span>

### <span data-ttu-id="fa7c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa7c8-114">-DefaultProfile</span></span>
<span data-ttu-id="fa7c8-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa7c8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa7c8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa7c8-116">-InputObject</span></span>
<span data-ttu-id="fa7c8-117">Eingabeobjekt für Piping</span><span class="sxs-lookup"><span data-stu-id="fa7c8-117">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa7c8-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fa7c8-118">-Name</span></span>
<span data-ttu-id="fa7c8-119">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="fa7c8-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa7c8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa7c8-120">-PassThru</span></span>
<span data-ttu-id="fa7c8-121">Gibt die gelöschten Kapazitätsdetails zurück, wenn der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="fa7c8-121">Will return the deleted capacity details if the operation completes successfully</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa7c8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa7c8-122">-ResourceGroupName</span></span>
<span data-ttu-id="fa7c8-123">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="fa7c8-123">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa7c8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa7c8-124">-ResourceId</span></span>
<span data-ttu-id="fa7c8-125">Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="fa7c8-125">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa7c8-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fa7c8-126">-Confirm</span></span>
<span data-ttu-id="fa7c8-127">Fordert den Benutzer auf, zu bestätigen, ob er den Vorgang ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="fa7c8-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="fa7c8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa7c8-128">-WhatIf</span></span>
<span data-ttu-id="fa7c8-129">Beschreibt die Aktionen, die der aktuelle Vorgang ausführen soll, ohne sie tatsächlich durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="fa7c8-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="fa7c8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa7c8-130">CommonParameters</span></span>
<span data-ttu-id="fa7c8-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa7c8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa7c8-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa7c8-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa7c8-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fa7c8-133">INPUTS</span></span>

### <span data-ttu-id="fa7c8-134">System.String</span><span class="sxs-lookup"><span data-stu-id="fa7c8-134">System.String</span></span>

### <span data-ttu-id="fa7c8-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="fa7c8-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="fa7c8-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fa7c8-136">OUTPUTS</span></span>

### <span data-ttu-id="fa7c8-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="fa7c8-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="fa7c8-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fa7c8-138">NOTES</span></span>

## <span data-ttu-id="fa7c8-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fa7c8-139">RELATED LINKS</span></span>

[<span data-ttu-id="fa7c8-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="fa7c8-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="fa7c8-141">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="fa7c8-141">New-AzPowerBIEmbeddedCapacity</span></span>](./New-AzPowerBIEmbeddedCapacity.md)
