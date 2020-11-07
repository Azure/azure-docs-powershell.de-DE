---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryHub.md
ms.openlocfilehash: 09e78957b3eef48731f2226a0737d0017c1e9b98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663185"
---
# <span data-ttu-id="fd870-101">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="fd870-101">Remove-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="fd870-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd870-102">SYNOPSIS</span></span>
<span data-ttu-id="fd870-103">Entfernt einen Hub aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="fd870-103">Removes a hub from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd870-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd870-104">SYNTAX</span></span>

### <span data-ttu-id="fd870-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd870-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd870-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fd870-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd870-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd870-107">DESCRIPTION</span></span>
<span data-ttu-id="fd870-108">Das Cmdlet **Remove-AzureRmDataFactoryHub** entfernt einen Hub aus Azure Data Factory in der angegebenen Azure-Ressourcengruppe und in der angegebenen Data Factory.</span><span class="sxs-lookup"><span data-stu-id="fd870-108">The **Remove-AzureRmDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="fd870-109">Wenn Sie einen Hub entfernen, werden alle verknüpften Dienste und Pipelines im Hub ebenfalls entfernt.</span><span class="sxs-lookup"><span data-stu-id="fd870-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="fd870-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd870-110">EXAMPLES</span></span>

### <span data-ttu-id="fd870-111">Beispiel 1: Entfernen eines Hubs</span><span class="sxs-lookup"><span data-stu-id="fd870-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="fd870-112">Dieser Befehl entfernt den Hub mit dem Namen ContosoDataHub aus der Azure-Ressourcengruppe mit dem Namen ADFResourceGroup und der Data Factory mit dem Namen ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="fd870-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="fd870-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd870-113">PARAMETERS</span></span>

### <span data-ttu-id="fd870-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fd870-114">-DataFactory</span></span>
<span data-ttu-id="fd870-115">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="fd870-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="fd870-116">Mit diesem Cmdlet wird ein Hub aus der Data Factory entfernt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fd870-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd870-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="fd870-117">-DataFactoryName</span></span>
<span data-ttu-id="fd870-118">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="fd870-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="fd870-119">Mit diesem Cmdlet wird ein Hub aus der Data Factory entfernt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fd870-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fd870-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd870-120">-DefaultProfile</span></span>
<span data-ttu-id="fd870-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="fd870-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd870-122">-Force</span><span class="sxs-lookup"><span data-stu-id="fd870-122">-Force</span></span>
<span data-ttu-id="fd870-123">Gibt an, dass dieses Cmdlet einen Hub entfernt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="fd870-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="fd870-124">-Name</span><span class="sxs-lookup"><span data-stu-id="fd870-124">-Name</span></span>
<span data-ttu-id="fd870-125">Gibt den Namen des zu entfernenden Hubs an.</span><span class="sxs-lookup"><span data-stu-id="fd870-125">Specifies the name of the hub to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd870-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd870-126">-ResourceGroupName</span></span>
<span data-ttu-id="fd870-127">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="fd870-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fd870-128">Mit diesem Cmdlet wird ein Hub aus der Gruppe entfernt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fd870-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fd870-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fd870-129">-Confirm</span></span>
<span data-ttu-id="fd870-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd870-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd870-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd870-131">-WhatIf</span></span>
<span data-ttu-id="fd870-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd870-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd870-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd870-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd870-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd870-134">CommonParameters</span></span>
<span data-ttu-id="fd870-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd870-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd870-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd870-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd870-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd870-137">INPUTS</span></span>

### <span data-ttu-id="fd870-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fd870-138">System.String</span></span>

### <span data-ttu-id="fd870-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fd870-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="fd870-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd870-140">OUTPUTS</span></span>

### <span data-ttu-id="fd870-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd870-141">System.Boolean</span></span>

## <span data-ttu-id="fd870-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd870-142">NOTES</span></span>
* <span data-ttu-id="fd870-143">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="fd870-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fd870-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd870-144">RELATED LINKS</span></span>

[<span data-ttu-id="fd870-145">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="fd870-145">Get-AzureRmDataFactoryHub</span></span>](./Get-AzureRmDataFactoryHub.md)

[<span data-ttu-id="fd870-146">Neu – AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="fd870-146">New-AzureRmDataFactoryHub</span></span>](./New-AzureRmDataFactoryHub.md)


