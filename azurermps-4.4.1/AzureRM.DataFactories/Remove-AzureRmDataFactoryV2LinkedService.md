---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: bba4df58ed4046eeba562e3438119e1d5df40649
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499141"
---
# <span data-ttu-id="d57a3-101">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="d57a3-101">Remove-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="d57a3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d57a3-102">SYNOPSIS</span></span>
<span data-ttu-id="d57a3-103">Entfernt einen verknüpften Dienst aus Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d57a3-103">Removes a linked service from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d57a3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d57a3-104">SYNTAX</span></span>

### <span data-ttu-id="d57a3-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d57a3-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d57a3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d57a3-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d57a3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d57a3-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d57a3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d57a3-108">DESCRIPTION</span></span>
<span data-ttu-id="d57a3-109">Das Remove-AzureRmDataFactoryV2LinkedService-Cmdlet entfernt einen verknüpften Dienst aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d57a3-109">The Remove-AzureRmDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="d57a3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d57a3-110">EXAMPLES</span></span>

### <span data-ttu-id="d57a3-111">Beispiel 1: Entfernen eines verknüpften Diensts</span><span class="sxs-lookup"><span data-stu-id="d57a3-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="d57a3-112">Mit diesem Befehl wird der verknüpfte Dienst mit dem Namen LinkedServiceTest aus der Data Factory mit dem Namen WikiADF entfernt.</span><span class="sxs-lookup"><span data-stu-id="d57a3-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="d57a3-113">Dieser Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="d57a3-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="d57a3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d57a3-114">PARAMETERS</span></span>

### <span data-ttu-id="d57a3-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d57a3-115">-Confirm</span></span>
<span data-ttu-id="d57a3-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d57a3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d57a3-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d57a3-117">-DataFactoryName</span></span>
<span data-ttu-id="d57a3-118">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="d57a3-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d57a3-119">Mit diesem Cmdlet wird ein verknüpfter Dienst aus der Data Factory entfernt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d57a3-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d57a3-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d57a3-120">-Force</span></span>
<span data-ttu-id="d57a3-121">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="d57a3-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d57a3-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d57a3-122">-InputObject</span></span>
<span data-ttu-id="d57a3-123">Gibt das zu entfernende LinkedService-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d57a3-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d57a3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d57a3-124">-Name</span></span>
<span data-ttu-id="d57a3-125">Gibt den Namen des zu entfernenden verknüpften Diensts an.</span><span class="sxs-lookup"><span data-stu-id="d57a3-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="d57a3-126">Der Name des verknüpften Diensts.</span><span class="sxs-lookup"><span data-stu-id="d57a3-126">Name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d57a3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d57a3-127">-ResourceGroupName</span></span>
<span data-ttu-id="d57a3-128">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d57a3-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d57a3-129">Mit diesem Cmdlet wird ein verknüpfter Dienst aus der Gruppe entfernt, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d57a3-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>


```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d57a3-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d57a3-130">-ResourceId</span></span>
<span data-ttu-id="d57a3-131">Die Azure-Ressourcen-ID des zu entfernenden verknüpften Diensts.</span><span class="sxs-lookup"><span data-stu-id="d57a3-131">The Azure resource ID of the linked service to remove.</span></span>

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

### <span data-ttu-id="d57a3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d57a3-132">-WhatIf</span></span>
<span data-ttu-id="d57a3-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d57a3-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d57a3-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d57a3-134">-DefaultProfile</span></span>
<span data-ttu-id="d57a3-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d57a3-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d57a3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d57a3-136">CommonParameters</span></span>
<span data-ttu-id="d57a3-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d57a3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d57a3-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d57a3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d57a3-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d57a3-139">INPUTS</span></span>

### <span data-ttu-id="d57a3-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="d57a3-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>
<span data-ttu-id="d57a3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d57a3-141">System.String</span></span>

## <span data-ttu-id="d57a3-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d57a3-142">OUTPUTS</span></span>

### <span data-ttu-id="d57a3-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="d57a3-143">System.Object</span></span>

## <span data-ttu-id="d57a3-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="d57a3-144">NOTES</span></span>
<span data-ttu-id="d57a3-145">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="d57a3-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d57a3-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d57a3-146">RELATED LINKS</span></span>

[<span data-ttu-id="d57a3-147">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="d57a3-147">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="d57a3-148">Satz-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="d57a3-148">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

