---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/update-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 22e6cf883268520f0568e28041f210268419a9a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369801"
---
# <span data-ttu-id="fc6d1-101">Update-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="fc6d1-101">Update-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="fc6d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc6d1-102">SYNOPSIS</span></span>
<span data-ttu-id="fc6d1-103">Ändert eine Instanz der eingebetteten PowerBI-Kapazität.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="fc6d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc6d1-104">SYNTAX</span></span>

### <span data-ttu-id="fc6d1-105">ByNameAndResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="fc6d1-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc6d1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fc6d1-106">ByResourceId</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc6d1-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fc6d1-107">ByInputObject</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc6d1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc6d1-108">DESCRIPTION</span></span>
<span data-ttu-id="fc6d1-109">Das Update-AzPowerBIEmbeddedCapacity ändert eine Instanz der eingebetteten PowerBI-Kapazität.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-109">The Update-AzPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="fc6d1-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fc6d1-110">EXAMPLES</span></span>

### <span data-ttu-id="fc6d1-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fc6d1-111">Example 1</span></span>
```
PS C:\> Update-AzPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com", "testuser2@contoso.com", "9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {testuser1@contoso.com, testuser2@contoso.com, 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {[key1, value1], [key2, value2]}
```

<span data-ttu-id="fc6d1-112">Ändert die Kapazitäts benannte Testkraft in der Ressourcengruppentestgruppe, um die Tags als "key1:value1" und "key2:value2" und "administrator" auf und den testuser1@contoso.com testuser2@contoso.com Dienstprinzipal zu setzen: 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span><span class="sxs-lookup"><span data-stu-id="fc6d1-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com , testuser2@contoso.com and the service principal: 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span></span>

## <span data-ttu-id="fc6d1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc6d1-113">PARAMETERS</span></span>

### <span data-ttu-id="fc6d1-114">-Administrator</span><span class="sxs-lookup"><span data-stu-id="fc6d1-114">-Administrator</span></span>
<span data-ttu-id="fc6d1-115">Durch Kommas getrennte Namen, die als Administratoren für die Kapazität festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-115">A comma separated names to set as administrators on the capacity.</span></span> <span data-ttu-id="fc6d1-116">Dienstprinzipal: <service principal object id>@<tenant id></span><span class="sxs-lookup"><span data-stu-id="fc6d1-116">For service principal: <service principal object id>@<tenant id></span></span>

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

### <span data-ttu-id="fc6d1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc6d1-117">-DefaultProfile</span></span>
<span data-ttu-id="fc6d1-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc6d1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc6d1-119">-InputObject</span></span>
<span data-ttu-id="fc6d1-120">Eingabeobjekt für die Pipierung</span><span class="sxs-lookup"><span data-stu-id="fc6d1-120">Input object for Piping</span></span>

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

### <span data-ttu-id="fc6d1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fc6d1-121">-Name</span></span>
<span data-ttu-id="fc6d1-122">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="fc6d1-122">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="fc6d1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc6d1-123">-PassThru</span></span>
<span data-ttu-id="fc6d1-124">Gibt die gelöschten Kapazitätsdetails zurück, wenn der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-124">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="fc6d1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc6d1-125">-ResourceGroupName</span></span>
<span data-ttu-id="fc6d1-126">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="fc6d1-126">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="fc6d1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc6d1-127">-ResourceId</span></span>
<span data-ttu-id="fc6d1-128">Eingebettete PowerBI-KapazitätsressourceID.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-128">PowerBI Embedded Capacity ResourceID.</span></span>

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

### <span data-ttu-id="fc6d1-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="fc6d1-129">-Sku</span></span>
<span data-ttu-id="fc6d1-130">Der Name der SKU für die Kapazität.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-130">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="fc6d1-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="fc6d1-131">-Tag</span></span>
<span data-ttu-id="fc6d1-132">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags für die Kapazität festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-132">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="fc6d1-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc6d1-133">-Confirm</span></span>
<span data-ttu-id="fc6d1-134">Fordert den Benutzer auf, zu bestätigen, ob er den Vorgang ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-134">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="fc6d1-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fc6d1-135">-WhatIf</span></span>
<span data-ttu-id="fc6d1-136">Beschreibt die Aktionen, die der aktuelle Vorgang ausführen wird, ohne sie tatsächlich durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-136">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="fc6d1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc6d1-137">CommonParameters</span></span>
<span data-ttu-id="fc6d1-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc6d1-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc6d1-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc6d1-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fc6d1-140">INPUTS</span></span>

### <span data-ttu-id="fc6d1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="fc6d1-141">System.String</span></span>

### <span data-ttu-id="fc6d1-142">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbedded1</span><span class="sxs-lookup"><span data-stu-id="fc6d1-142">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="fc6d1-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fc6d1-143">OUTPUTS</span></span>

### <span data-ttu-id="fc6d1-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbedded1</span><span class="sxs-lookup"><span data-stu-id="fc6d1-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="fc6d1-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fc6d1-145">NOTES</span></span>

## <span data-ttu-id="fc6d1-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fc6d1-146">RELATED LINKS</span></span>

[<span data-ttu-id="fc6d1-147">Get-AzPowerBIEmbedded1</span><span class="sxs-lookup"><span data-stu-id="fc6d1-147">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="fc6d1-148">Remove-AzPowerBIEmbedded1</span><span class="sxs-lookup"><span data-stu-id="fc6d1-148">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
