---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryHub.md
ms.openlocfilehash: 891debe69749b67277e2ba24e439fe43143b71c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664350"
---
# <span data-ttu-id="3f226-101">New-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="3f226-101">New-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="3f226-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f226-102">SYNOPSIS</span></span>
<span data-ttu-id="3f226-103">Erstellt einen Hub für eine Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="3f226-103">Creates a hub for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f226-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f226-104">SYNTAX</span></span>

### <span data-ttu-id="3f226-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3f226-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f226-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3f226-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f226-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f226-107">DESCRIPTION</span></span>
<span data-ttu-id="3f226-108">Das Cmdlet **New-AzureRmDataFactoryHub** erstellt einen Hub für Azure Data Factory in der angegebenen Azure-Ressourcengruppe und in der angegebenen Data Factory mit der angegebenen Datei Definition.</span><span class="sxs-lookup"><span data-stu-id="3f226-108">The **New-AzureRmDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="3f226-109">Nachdem Sie den Hub erstellt haben, können Sie ihn zum Speichern und verwalten verknüpfter Dienste in einer Gruppe verwenden, und Sie können dem Hub Pipelines hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3f226-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="3f226-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f226-110">EXAMPLES</span></span>

### <span data-ttu-id="3f226-111">Beispiel 1: Erstellen eines Hubs</span><span class="sxs-lookup"><span data-stu-id="3f226-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="3f226-112">Dieser Befehl erstellt einen Hub mit dem Namen ContosoDataHub in der Ressourcengruppe ADFResourceGroup und der Data Factory mit dem Namen ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="3f226-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="3f226-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f226-113">PARAMETERS</span></span>

### <span data-ttu-id="3f226-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f226-114">-DataFactory</span></span>
<span data-ttu-id="3f226-115">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3f226-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="3f226-116">Dieses Cmdlet erstellt einen Hub für die Data Factory, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="3f226-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3f226-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="3f226-117">-DataFactoryName</span></span>
<span data-ttu-id="3f226-118">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="3f226-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3f226-119">Dieses Cmdlet erstellt einen Hub für die Data Factory, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="3f226-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3f226-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f226-120">-DefaultProfile</span></span>
<span data-ttu-id="3f226-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3f226-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f226-122">-Datei</span><span class="sxs-lookup"><span data-stu-id="3f226-122">-File</span></span>
<span data-ttu-id="3f226-123">Gibt den vollständigen Pfad der JSON-Datei (JavaScript Object Notation) an, die die Beschreibung des Hubs enthält.</span><span class="sxs-lookup"><span data-stu-id="3f226-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f226-124">-Force</span><span class="sxs-lookup"><span data-stu-id="3f226-124">-Force</span></span>
<span data-ttu-id="3f226-125">Gibt an, dass dieses Cmdlet einen vorhandenen Hub ersetzt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="3f226-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="3f226-126">-Name</span><span class="sxs-lookup"><span data-stu-id="3f226-126">-Name</span></span>
<span data-ttu-id="3f226-127">Gibt den Namen des zu erstellenden Hubs an.</span><span class="sxs-lookup"><span data-stu-id="3f226-127">Specifies the name of the hub to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f226-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f226-128">-ResourceGroupName</span></span>
<span data-ttu-id="3f226-129">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3f226-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3f226-130">Mit diesem Cmdlet wird ein Hub erstellt, der zu der Gruppe gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="3f226-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3f226-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3f226-131">-Confirm</span></span>
<span data-ttu-id="3f226-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f226-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f226-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f226-133">-WhatIf</span></span>
<span data-ttu-id="3f226-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f226-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f226-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f226-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f226-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f226-136">CommonParameters</span></span>
<span data-ttu-id="3f226-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f226-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f226-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f226-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f226-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f226-139">INPUTS</span></span>

### <span data-ttu-id="3f226-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3f226-140">System.String</span></span>

### <span data-ttu-id="3f226-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3f226-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="3f226-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f226-142">OUTPUTS</span></span>

### <span data-ttu-id="3f226-143">Microsoft. Azure. Commands. datafactoring. Models. PSHub</span><span class="sxs-lookup"><span data-stu-id="3f226-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="3f226-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f226-144">NOTES</span></span>
* <span data-ttu-id="3f226-145">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="3f226-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3f226-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f226-146">RELATED LINKS</span></span>

[<span data-ttu-id="3f226-147">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="3f226-147">Get-AzureRmDataFactoryHub</span></span>](./Get-AzureRmDataFactoryHub.md)

[<span data-ttu-id="3f226-148">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="3f226-148">Remove-AzureRmDataFactoryHub</span></span>](./Remove-AzureRmDataFactoryHub.md)


