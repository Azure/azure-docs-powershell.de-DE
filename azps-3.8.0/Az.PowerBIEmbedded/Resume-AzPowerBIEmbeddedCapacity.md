---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/resume-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4fdb8845b59a57b20813f92e3858cc7c54310d23
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003749"
---
# <span data-ttu-id="1df2c-101">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1df2c-101">Resume-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="1df2c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1df2c-102">SYNOPSIS</span></span>
<span data-ttu-id="1df2c-103">Setzt eine Instanz der eingebetteten PowerBI-Kapazität fort.</span><span class="sxs-lookup"><span data-stu-id="1df2c-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="1df2c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1df2c-104">SYNTAX</span></span>

### <span data-ttu-id="1df2c-105">ByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="1df2c-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1df2c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1df2c-106">ByResourceId</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1df2c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1df2c-107">ByInputObject</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1df2c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1df2c-108">DESCRIPTION</span></span>
<span data-ttu-id="1df2c-109">Das Resume-AzPowerBIEmbeddedCapacity-Cmdlet setzt eine Instanz der eingebetteten PowerBI-Kapazität fort</span><span class="sxs-lookup"><span data-stu-id="1df2c-109">The Resume-AzPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="1df2c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1df2c-110">EXAMPLES</span></span>

### <span data-ttu-id="1df2c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1df2c-111">Example 1</span></span>
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

<span data-ttu-id="1df2c-112">Dieser Befehl setzt eine angehaltene Kapazität mit dem Namen testcapacity in der testRG</span><span class="sxs-lookup"><span data-stu-id="1df2c-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="1df2c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1df2c-113">PARAMETERS</span></span>

### <span data-ttu-id="1df2c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1df2c-114">-DefaultProfile</span></span>
<span data-ttu-id="1df2c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1df2c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1df2c-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1df2c-116">-InputObject</span></span>
<span data-ttu-id="1df2c-117">Eingabeobjekt für die Rohrverlegung</span><span class="sxs-lookup"><span data-stu-id="1df2c-117">Input object for Piping</span></span>

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

### <span data-ttu-id="1df2c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1df2c-118">-Name</span></span>
<span data-ttu-id="1df2c-119">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="1df2c-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="1df2c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1df2c-120">-PassThru</span></span>
<span data-ttu-id="1df2c-121">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="1df2c-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1df2c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1df2c-122">-ResourceGroupName</span></span>
<span data-ttu-id="1df2c-123">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="1df2c-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="1df2c-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1df2c-124">-ResourceId</span></span>
<span data-ttu-id="1df2c-125">Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="1df2c-125">Azure resource ID</span></span>

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

### <span data-ttu-id="1df2c-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1df2c-126">-Confirm</span></span>
<span data-ttu-id="1df2c-127">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="1df2c-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="1df2c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1df2c-128">-WhatIf</span></span>
<span data-ttu-id="1df2c-129">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="1df2c-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="1df2c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1df2c-130">CommonParameters</span></span>
<span data-ttu-id="1df2c-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1df2c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1df2c-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1df2c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1df2c-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1df2c-133">INPUTS</span></span>

### <span data-ttu-id="1df2c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1df2c-134">System.String</span></span>

### <span data-ttu-id="1df2c-135">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1df2c-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="1df2c-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1df2c-136">OUTPUTS</span></span>

### <span data-ttu-id="1df2c-137">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1df2c-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="1df2c-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="1df2c-138">NOTES</span></span>

## <span data-ttu-id="1df2c-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1df2c-139">RELATED LINKS</span></span>

[<span data-ttu-id="1df2c-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1df2c-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="1df2c-141">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1df2c-141">Suspend-AzPowerBIEmbeddedCapacity</span></span>](./Suspend-AzPowerBIEmbeddedCapacity.md)
