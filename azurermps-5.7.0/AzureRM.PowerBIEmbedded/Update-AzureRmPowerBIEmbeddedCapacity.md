---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/update-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 64e96f423748e8991abcf26b178a8bd6b893cf0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476694"
---
# <span data-ttu-id="b86bc-101">Update-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="b86bc-101">Update-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="b86bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b86bc-102">SYNOPSIS</span></span>
<span data-ttu-id="b86bc-103">Ändert eine Instanz der eingebetteten PowerBI-Kapazität.</span><span class="sxs-lookup"><span data-stu-id="b86bc-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b86bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b86bc-104">SYNTAX</span></span>

```
Update-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [[-Sku] <String>]
    [[-Tag] <Hashtable>] 
    [[-Administrator] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="b86bc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b86bc-105">DESCRIPTION</span></span>
<span data-ttu-id="b86bc-106">Das Update-AzureRmPowerBIEmbeddedCapacity-Cmdlet ändert eine Instanz der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="b86bc-106">The Update-AzureRmPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="b86bc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b86bc-107">EXAMPLES</span></span>

### <span data-ttu-id="b86bc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b86bc-108">Example 1</span></span>
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

<span data-ttu-id="b86bc-109">Ändert die Kapazität mit dem Namen "testcapacity" in der ResourceGroup-Testgruppe, um die Tags als key1: value1 und key2: Value2 und Administrator auf testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="b86bc-109">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="b86bc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b86bc-110">PARAMETERS</span></span>

### <span data-ttu-id="b86bc-111">-Name</span><span class="sxs-lookup"><span data-stu-id="b86bc-111">-Name</span></span>
<span data-ttu-id="b86bc-112">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="b86bc-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="b86bc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b86bc-113">-ResourceGroupName</span></span>
<span data-ttu-id="b86bc-114">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="b86bc-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="b86bc-115">-SKU</span><span class="sxs-lookup"><span data-stu-id="b86bc-115">-Sku</span></span>
<span data-ttu-id="b86bc-116">Der Name der SKU für die Kapazität.</span><span class="sxs-lookup"><span data-stu-id="b86bc-116">The name of the Sku for the capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: A1, A2, A3, A4, A5, A6

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="b86bc-117">-Tag</span><span class="sxs-lookup"><span data-stu-id="b86bc-117">-Tag</span></span>
<span data-ttu-id="b86bc-118">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags für die Kapazität definiert ist.</span><span class="sxs-lookup"><span data-stu-id="b86bc-118">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```
### <span data-ttu-id="b86bc-119">– Administrator</span><span class="sxs-lookup"><span data-stu-id="b86bc-119">-Administrator</span></span>
<span data-ttu-id="b86bc-120">Eine durch Kommas getrennte Kapazitäts Namen, die als Administrator auf der Kapazität eingestellt werden</span><span class="sxs-lookup"><span data-stu-id="b86bc-120">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="b86bc-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b86bc-121">-ResourceId</span></span>
<span data-ttu-id="b86bc-122">PowerBI eingebettete Kapazitäts-Kapazitäts-Nr.</span><span class="sxs-lookup"><span data-stu-id="b86bc-122">PowerBI Embedded Capacity ResourceID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b86bc-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b86bc-123">-InputObject</span></span>
<span data-ttu-id="b86bc-124">Eingabeobjekt für die Rohrverlegung</span><span class="sxs-lookup"><span data-stu-id="b86bc-124">Input object for Piping</span></span>

```yaml
Type: PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b86bc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b86bc-125">-PassThru</span></span>
<span data-ttu-id="b86bc-126">Gibt die gelöschten Kapazitätsdetails zurück, wenn der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="b86bc-126">Will return the deleted capacity details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b86bc-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b86bc-127">-Confirm</span></span>
<span data-ttu-id="b86bc-128">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="b86bc-128">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b86bc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b86bc-129">-WhatIf</span></span>
<span data-ttu-id="b86bc-130">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="b86bc-130">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b86bc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b86bc-131">CommonParameters</span></span>
<span data-ttu-id="b86bc-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b86bc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b86bc-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b86bc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b86bc-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b86bc-134">INPUTS</span></span>

### <span data-ttu-id="b86bc-135">Keine</span><span class="sxs-lookup"><span data-stu-id="b86bc-135">None</span></span>
<span data-ttu-id="b86bc-136">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="b86bc-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b86bc-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b86bc-137">OUTPUTS</span></span>

### <span data-ttu-id="b86bc-138">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="b86bc-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="b86bc-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="b86bc-139">NOTES</span></span>

## <span data-ttu-id="b86bc-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b86bc-140">RELATED LINKS</span></span>

[<span data-ttu-id="b86bc-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="b86bc-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="b86bc-142">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="b86bc-142">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
