---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/resume-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: cd0eab8d5670f8c37d45c8e0e211100749aa7a4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950696"
---
# <span data-ttu-id="e072b-101">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e072b-101">Resume-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e072b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e072b-102">SYNOPSIS</span></span>
<span data-ttu-id="e072b-103">Setzt eine Instanz der eingebetteten PowerBI-Kapazität fort.</span><span class="sxs-lookup"><span data-stu-id="e072b-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="e072b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e072b-104">SYNTAX</span></span>

### <span data-ttu-id="e072b-105">ByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="e072b-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e072b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e072b-106">ByResourceId</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e072b-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e072b-107">ByInputObject</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e072b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e072b-108">DESCRIPTION</span></span>
<span data-ttu-id="e072b-109">Das Resume-AzPowerBIEmbeddedCapacity-Cmdlet setzt eine Instanz der eingebetteten PowerBI-Kapazität fort.</span><span class="sxs-lookup"><span data-stu-id="e072b-109">The Resume-AzPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="e072b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e072b-110">EXAMPLES</span></span>

### <span data-ttu-id="e072b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e072b-111">Example 1</span></span>
```
PS C:\> Resume-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="e072b-112">Mit diesem Befehl wird eine angehaltene Kapazität namens Testkapazität im RessourcengruppentestRG fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="e072b-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="e072b-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e072b-113">PARAMETERS</span></span>

### <span data-ttu-id="e072b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e072b-114">-DefaultProfile</span></span>
<span data-ttu-id="e072b-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e072b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e072b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e072b-116">-InputObject</span></span>
<span data-ttu-id="e072b-117">Eingabeobjekt für Piping</span><span class="sxs-lookup"><span data-stu-id="e072b-117">Input object for Piping</span></span>

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

### <span data-ttu-id="e072b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e072b-118">-Name</span></span>
<span data-ttu-id="e072b-119">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="e072b-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="e072b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e072b-120">-PassThru</span></span>
<span data-ttu-id="e072b-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e072b-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e072b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e072b-122">-ResourceGroupName</span></span>
<span data-ttu-id="e072b-123">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="e072b-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="e072b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e072b-124">-ResourceId</span></span>
<span data-ttu-id="e072b-125">Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e072b-125">Azure resource ID</span></span>

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

### <span data-ttu-id="e072b-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e072b-126">-Confirm</span></span>
<span data-ttu-id="e072b-127">Fordert den Benutzer auf, zu bestätigen, ob er den Vorgang ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="e072b-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="e072b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e072b-128">-WhatIf</span></span>
<span data-ttu-id="e072b-129">Beschreibt die Aktionen, die der aktuelle Vorgang ausführen soll, ohne sie tatsächlich durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="e072b-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="e072b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e072b-130">CommonParameters</span></span>
<span data-ttu-id="e072b-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e072b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e072b-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e072b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e072b-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e072b-133">INPUTS</span></span>

### <span data-ttu-id="e072b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e072b-134">System.String</span></span>

### <span data-ttu-id="e072b-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e072b-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e072b-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e072b-136">OUTPUTS</span></span>

### <span data-ttu-id="e072b-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e072b-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e072b-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e072b-138">NOTES</span></span>

## <span data-ttu-id="e072b-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e072b-139">RELATED LINKS</span></span>

[<span data-ttu-id="e072b-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e072b-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="e072b-141">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e072b-141">Suspend-AzPowerBIEmbeddedCapacity</span></span>](./Suspend-AzPowerBIEmbeddedCapacity.md)
