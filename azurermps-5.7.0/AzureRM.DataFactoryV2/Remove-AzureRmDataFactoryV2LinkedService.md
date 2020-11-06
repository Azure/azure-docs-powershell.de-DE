---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: a636dcfabe3f1736f9705724ed302ab40d3637a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476825"
---
# <span data-ttu-id="03def-101">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="03def-101">Remove-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="03def-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="03def-102">SYNOPSIS</span></span>
<span data-ttu-id="03def-103">Entfernt einen verknüpften Dienst aus Data Factory.</span><span class="sxs-lookup"><span data-stu-id="03def-103">Removes a linked service from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03def-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="03def-104">SYNTAX</span></span>

### <span data-ttu-id="03def-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="03def-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03def-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="03def-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03def-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="03def-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03def-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03def-108">DESCRIPTION</span></span>
<span data-ttu-id="03def-109">Das Remove-AzureRmDataFactoryV2LinkedService-Cmdlet entfernt einen verknüpften Dienst aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="03def-109">The Remove-AzureRmDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="03def-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="03def-110">EXAMPLES</span></span>

### <span data-ttu-id="03def-111">Beispiel 1: Entfernen eines verknüpften Diensts</span><span class="sxs-lookup"><span data-stu-id="03def-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="03def-112">Mit diesem Befehl wird der verknüpfte Dienst mit dem Namen LinkedServiceTest aus der Data Factory mit dem Namen WikiADF entfernt.</span><span class="sxs-lookup"><span data-stu-id="03def-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="03def-113">Dieser Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="03def-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="03def-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="03def-114">PARAMETERS</span></span>

### <span data-ttu-id="03def-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="03def-115">-DataFactoryName</span></span>
<span data-ttu-id="03def-116">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="03def-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="03def-117">Mit diesem Cmdlet wird ein verknüpfter Dienst aus der Data Factory entfernt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="03def-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03def-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03def-118">-DefaultProfile</span></span>
<span data-ttu-id="03def-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="03def-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03def-120">-Force</span><span class="sxs-lookup"><span data-stu-id="03def-120">-Force</span></span>
<span data-ttu-id="03def-121">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="03def-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="03def-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="03def-122">-InputObject</span></span>
<span data-ttu-id="03def-123">Gibt das zu entfernende LinkedService-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="03def-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: PSLinkedService
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03def-124">-Name</span><span class="sxs-lookup"><span data-stu-id="03def-124">-Name</span></span>
<span data-ttu-id="03def-125">Gibt den Namen des zu entfernenden verknüpften Diensts an.</span><span class="sxs-lookup"><span data-stu-id="03def-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="03def-126">Der Name des verknüpften Diensts.</span><span class="sxs-lookup"><span data-stu-id="03def-126">Name of the linked service.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03def-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03def-127">-ResourceGroupName</span></span>
<span data-ttu-id="03def-128">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="03def-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="03def-129">Mit diesem Cmdlet wird ein verknüpfter Dienst aus der Gruppe entfernt, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="03def-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>


```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03def-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="03def-130">-ResourceId</span></span>
<span data-ttu-id="03def-131">Die Azure-Ressourcen-ID des zu entfernenden verknüpften Diensts.</span><span class="sxs-lookup"><span data-stu-id="03def-131">The Azure resource ID of the linked service to remove.</span></span>

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

### <span data-ttu-id="03def-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="03def-132">-Confirm</span></span>
<span data-ttu-id="03def-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="03def-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03def-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03def-134">-WhatIf</span></span>
<span data-ttu-id="03def-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="03def-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="03def-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03def-136">CommonParameters</span></span>
<span data-ttu-id="03def-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03def-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03def-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03def-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03def-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="03def-139">INPUTS</span></span>

### <span data-ttu-id="03def-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="03def-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>
<span data-ttu-id="03def-141">System. String</span><span class="sxs-lookup"><span data-stu-id="03def-141">System.String</span></span>

## <span data-ttu-id="03def-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="03def-142">OUTPUTS</span></span>

### <span data-ttu-id="03def-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="03def-143">System.Object</span></span>

## <span data-ttu-id="03def-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="03def-144">NOTES</span></span>
<span data-ttu-id="03def-145">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="03def-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="03def-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="03def-146">RELATED LINKS</span></span>

[<span data-ttu-id="03def-147">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="03def-147">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="03def-148">Satz-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="03def-148">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

