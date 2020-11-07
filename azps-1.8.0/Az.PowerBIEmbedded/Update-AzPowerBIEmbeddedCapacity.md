---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/update-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: bed116bedbd06919728da8727cad609813bfc2a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659994"
---
# <span data-ttu-id="e1808-101">Update-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e1808-101">Update-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e1808-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1808-102">SYNOPSIS</span></span>
<span data-ttu-id="e1808-103">Ändert eine Instanz der eingebetteten PowerBI-Kapazität.</span><span class="sxs-lookup"><span data-stu-id="e1808-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="e1808-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1808-104">SYNTAX</span></span>

### <span data-ttu-id="e1808-105">ByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="e1808-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1808-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e1808-106">ByResourceId</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1808-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e1808-107">ByInputObject</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1808-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1808-108">DESCRIPTION</span></span>
<span data-ttu-id="e1808-109">Das Update-AzPowerBIEmbeddedCapacity-Cmdlet ändert eine Instanz der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="e1808-109">The Update-AzPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="e1808-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1808-110">EXAMPLES</span></span>

### <span data-ttu-id="e1808-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e1808-111">Example 1</span></span>
```
PS C:\> Update-AzPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com, testuser2@contoso.com" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {testuser1@contoso.com, testuser2@contoso.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {[key1, value1], [key2, value2]}
```

<span data-ttu-id="e1808-112">Ändert die Kapazität mit dem Namen "testcapacity" in der ResourceGroup-Testgruppe, um die Tags als key1: value1 und key2: Value2 und Administrator auf testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="e1808-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="e1808-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1808-113">PARAMETERS</span></span>

### <span data-ttu-id="e1808-114">– Administrator</span><span class="sxs-lookup"><span data-stu-id="e1808-114">-Administrator</span></span>
<span data-ttu-id="e1808-115">Eine durch Kommas getrennte Kapazitäts Namen, die als Administrator auf der Kapazität eingestellt werden</span><span class="sxs-lookup"><span data-stu-id="e1808-115">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1808-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1808-116">-DefaultProfile</span></span>
<span data-ttu-id="e1808-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e1808-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1808-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e1808-118">-InputObject</span></span>
<span data-ttu-id="e1808-119">Eingabeobjekt für die Rohrverlegung</span><span class="sxs-lookup"><span data-stu-id="e1808-119">Input object for Piping</span></span>

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

### <span data-ttu-id="e1808-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e1808-120">-Name</span></span>
<span data-ttu-id="e1808-121">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="e1808-121">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="e1808-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1808-122">-PassThru</span></span>
<span data-ttu-id="e1808-123">Gibt die gelöschten Kapazitätsdetails zurück, wenn der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="e1808-123">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="e1808-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1808-124">-ResourceGroupName</span></span>
<span data-ttu-id="e1808-125">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="e1808-125">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="e1808-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e1808-126">-ResourceId</span></span>
<span data-ttu-id="e1808-127">PowerBI eingebettete Kapazitäts-Kapazitäts-Nr.</span><span class="sxs-lookup"><span data-stu-id="e1808-127">PowerBI Embedded Capacity ResourceID.</span></span>

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

### <span data-ttu-id="e1808-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="e1808-128">-Sku</span></span>
<span data-ttu-id="e1808-129">Der Name der SKU für die Kapazität.</span><span class="sxs-lookup"><span data-stu-id="e1808-129">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1808-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="e1808-130">-Tag</span></span>
<span data-ttu-id="e1808-131">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags für die Kapazität definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e1808-131">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1808-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e1808-132">-Confirm</span></span>
<span data-ttu-id="e1808-133">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="e1808-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="e1808-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1808-134">-WhatIf</span></span>
<span data-ttu-id="e1808-135">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="e1808-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="e1808-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1808-136">CommonParameters</span></span>
<span data-ttu-id="e1808-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1808-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1808-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1808-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1808-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1808-139">INPUTS</span></span>

### <span data-ttu-id="e1808-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e1808-140">System.String</span></span>

### <span data-ttu-id="e1808-141">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e1808-141">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e1808-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1808-142">OUTPUTS</span></span>

### <span data-ttu-id="e1808-143">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e1808-143">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e1808-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1808-144">NOTES</span></span>

## <span data-ttu-id="e1808-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1808-145">RELATED LINKS</span></span>

[<span data-ttu-id="e1808-146">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e1808-146">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="e1808-147">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e1808-147">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
