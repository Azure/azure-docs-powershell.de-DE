---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: c2dc0333d2e991b21ac1a921465971f2131f5c3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500157"
---
# <span data-ttu-id="2a367-101">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2a367-101">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="2a367-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2a367-102">SYNOPSIS</span></span>
<span data-ttu-id="2a367-103">Löscht eine Instanz der eingebetteten PowerBI-Kapazität.</span><span class="sxs-lookup"><span data-stu-id="2a367-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a367-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a367-104">SYNTAX</span></span>

### <span data-ttu-id="2a367-105">ByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="2a367-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a367-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2a367-106">ByResourceId</span></span>
```
Remove-AzureRmPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a367-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2a367-107">ByInputObject</span></span>
```
Remove-AzureRmPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a367-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2a367-108">DESCRIPTION</span></span>
<span data-ttu-id="2a367-109">Das Remove-AzureRmPowerBIEmbeddedCapacity-Cmdlet löscht eine Instanz der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="2a367-109">The Remove-AzureRmPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="2a367-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2a367-110">EXAMPLES</span></span>

### <span data-ttu-id="2a367-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2a367-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
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

<span data-ttu-id="2a367-112">Dieser Befehl entfernt die Kapazität mit dem Namen testcapacity in der testRG</span><span class="sxs-lookup"><span data-stu-id="2a367-112">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="2a367-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a367-113">PARAMETERS</span></span>

### <span data-ttu-id="2a367-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a367-114">-DefaultProfile</span></span>
<span data-ttu-id="2a367-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2a367-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a367-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2a367-116">-InputObject</span></span>
<span data-ttu-id="2a367-117">Eingabeobjekt für die Rohrverlegung</span><span class="sxs-lookup"><span data-stu-id="2a367-117">Input object for Piping</span></span>

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

### <span data-ttu-id="2a367-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2a367-118">-Name</span></span>
<span data-ttu-id="2a367-119">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="2a367-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="2a367-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a367-120">-PassThru</span></span>
<span data-ttu-id="2a367-121">Gibt die gelöschten Kapazitätsdetails zurück, wenn der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="2a367-121">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="2a367-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a367-122">-ResourceGroupName</span></span>
<span data-ttu-id="2a367-123">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="2a367-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="2a367-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2a367-124">-ResourceId</span></span>
<span data-ttu-id="2a367-125">Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2a367-125">Azure resource ID</span></span>

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

### <span data-ttu-id="2a367-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2a367-126">-Confirm</span></span>
<span data-ttu-id="2a367-127">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="2a367-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="2a367-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a367-128">-WhatIf</span></span>
<span data-ttu-id="2a367-129">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="2a367-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="2a367-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a367-130">CommonParameters</span></span>
<span data-ttu-id="2a367-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a367-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a367-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a367-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a367-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2a367-133">INPUTS</span></span>

### <span data-ttu-id="2a367-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2a367-134">System.String</span></span>

### <span data-ttu-id="2a367-135">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2a367-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="2a367-136">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2a367-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2a367-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2a367-137">OUTPUTS</span></span>

### <span data-ttu-id="2a367-138">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2a367-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="2a367-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="2a367-139">NOTES</span></span>

## <span data-ttu-id="2a367-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2a367-140">RELATED LINKS</span></span>

[<span data-ttu-id="2a367-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2a367-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="2a367-142">Neu – AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2a367-142">New-AzureRmPowerBIEmbeddedCapacity</span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)
