---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/update-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 6236a03b22bd3509933d58579db3e84d48723b68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503458"
---
# <span data-ttu-id="7bb14-101">Update-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7bb14-101">Update-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="7bb14-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7bb14-102">SYNOPSIS</span></span>
<span data-ttu-id="7bb14-103">Ändert eine Instanz der eingebetteten PowerBI-Kapazität.</span><span class="sxs-lookup"><span data-stu-id="7bb14-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bb14-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bb14-104">SYNTAX</span></span>

### <span data-ttu-id="7bb14-105">ByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="7bb14-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bb14-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7bb14-106">ByResourceId</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7bb14-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7bb14-107">ByInputObject</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bb14-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7bb14-108">DESCRIPTION</span></span>
<span data-ttu-id="7bb14-109">Das Update-AzureRmPowerBIEmbeddedCapacity-Cmdlet ändert eine Instanz der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="7bb14-109">The Update-AzureRmPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="7bb14-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7bb14-110">EXAMPLES</span></span>

### <span data-ttu-id="7bb14-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7bb14-111">Example 1</span></span>
```
PS C:\> Update-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com, testuser2@contoso.com" -PassThru
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

<span data-ttu-id="7bb14-112">Ändert die Kapazität mit dem Namen "testcapacity" in der ResourceGroup-Testgruppe, um die Tags als key1: value1 und key2: Value2 und Administrator auf testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="7bb14-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="7bb14-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bb14-113">PARAMETERS</span></span>

### <span data-ttu-id="7bb14-114">– Administrator</span><span class="sxs-lookup"><span data-stu-id="7bb14-114">-Administrator</span></span>
<span data-ttu-id="7bb14-115">Eine durch Kommas getrennte Kapazitäts Namen, die als Administrator auf der Kapazität eingestellt werden</span><span class="sxs-lookup"><span data-stu-id="7bb14-115">A comma separated capacity names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="7bb14-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bb14-116">-DefaultProfile</span></span>
<span data-ttu-id="7bb14-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7bb14-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bb14-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7bb14-118">-InputObject</span></span>
<span data-ttu-id="7bb14-119">Eingabeobjekt für die Rohrverlegung</span><span class="sxs-lookup"><span data-stu-id="7bb14-119">Input object for Piping</span></span>

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

### <span data-ttu-id="7bb14-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7bb14-120">-Name</span></span>
<span data-ttu-id="7bb14-121">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="7bb14-121">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="7bb14-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7bb14-122">-PassThru</span></span>
<span data-ttu-id="7bb14-123">Gibt die gelöschten Kapazitätsdetails zurück, wenn der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="7bb14-123">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="7bb14-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bb14-124">-ResourceGroupName</span></span>
<span data-ttu-id="7bb14-125">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="7bb14-125">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="7bb14-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7bb14-126">-ResourceId</span></span>
<span data-ttu-id="7bb14-127">PowerBI eingebettete Kapazitäts-Kapazitäts-Nr.</span><span class="sxs-lookup"><span data-stu-id="7bb14-127">PowerBI Embedded Capacity ResourceID.</span></span>

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

### <span data-ttu-id="7bb14-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="7bb14-128">-Sku</span></span>
<span data-ttu-id="7bb14-129">Der Name der SKU für die Kapazität.</span><span class="sxs-lookup"><span data-stu-id="7bb14-129">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="7bb14-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="7bb14-130">-Tag</span></span>
<span data-ttu-id="7bb14-131">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags für die Kapazität definiert ist.</span><span class="sxs-lookup"><span data-stu-id="7bb14-131">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="7bb14-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7bb14-132">-Confirm</span></span>
<span data-ttu-id="7bb14-133">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="7bb14-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="7bb14-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bb14-134">-WhatIf</span></span>
<span data-ttu-id="7bb14-135">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="7bb14-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="7bb14-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bb14-136">CommonParameters</span></span>
<span data-ttu-id="7bb14-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bb14-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bb14-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bb14-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bb14-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7bb14-139">INPUTS</span></span>

### <span data-ttu-id="7bb14-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7bb14-140">System.String</span></span>

### <span data-ttu-id="7bb14-141">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7bb14-141">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="7bb14-142">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7bb14-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="7bb14-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7bb14-143">OUTPUTS</span></span>

### <span data-ttu-id="7bb14-144">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7bb14-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="7bb14-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="7bb14-145">NOTES</span></span>

## <span data-ttu-id="7bb14-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7bb14-146">RELATED LINKS</span></span>

[<span data-ttu-id="7bb14-147">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7bb14-147">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="7bb14-148">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7bb14-148">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
