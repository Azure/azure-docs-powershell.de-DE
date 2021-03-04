---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
ms.openlocfilehash: 91e1bb556f2464f535e64a870b5491fceb9eac4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928248"
---
# <span data-ttu-id="58c46-101">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="58c46-101">New-AzDataFactoryHub</span></span>

## <span data-ttu-id="58c46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58c46-102">SYNOPSIS</span></span>
<span data-ttu-id="58c46-103">Erstellt einen Hub für eine Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="58c46-103">Creates a hub for an Azure Data Factory.</span></span>

## <span data-ttu-id="58c46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58c46-104">SYNTAX</span></span>

### <span data-ttu-id="58c46-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="58c46-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58c46-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="58c46-106">ByFactoryObject</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58c46-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58c46-107">DESCRIPTION</span></span>
<span data-ttu-id="58c46-108">Das **Cmdlet New-AzDataFactoryHub** erstellt einen Hub für Azure Data Factory in der angegebenen Azure-Ressourcengruppe und in der angegebenen Datenfactory mit der angegebenen Dateidefinition.</span><span class="sxs-lookup"><span data-stu-id="58c46-108">The **New-AzDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="58c46-109">Nachdem Sie den Hub erstellt haben, können Sie ihn verwenden, um verknüpfte Dienste in einer Gruppe zu speichern und zu verwalten, und Sie können dem Hub Pipelines hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="58c46-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="58c46-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="58c46-110">EXAMPLES</span></span>

### <span data-ttu-id="58c46-111">Beispiel 1: Erstellen eines Hubs</span><span class="sxs-lookup"><span data-stu-id="58c46-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="58c46-112">Mit diesem Befehl wird ein Hub namens ContosoDataHub in der Ressourcengruppe ADFResourceGroup und der Datenfactory mit dem Namen ADFDataFactory erstellt.</span><span class="sxs-lookup"><span data-stu-id="58c46-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="58c46-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="58c46-113">PARAMETERS</span></span>

### <span data-ttu-id="58c46-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="58c46-114">-DataFactory</span></span>
<span data-ttu-id="58c46-115">Gibt ein **PSDataFactory-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="58c46-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="58c46-116">Dieses Cmdlet erstellt einen Hub für die Daten factory, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="58c46-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="58c46-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="58c46-117">-DataFactoryName</span></span>
<span data-ttu-id="58c46-118">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="58c46-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="58c46-119">Dieses Cmdlet erstellt einen Hub für die Daten factory, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="58c46-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="58c46-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c46-120">-DefaultProfile</span></span>
<span data-ttu-id="58c46-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="58c46-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58c46-122">-Datei</span><span class="sxs-lookup"><span data-stu-id="58c46-122">-File</span></span>
<span data-ttu-id="58c46-123">Gibt den vollständigen Pfad der JSON(JavaScript Object Notation)-Datei an, die die Beschreibung des Hubs enthält.</span><span class="sxs-lookup"><span data-stu-id="58c46-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

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

### <span data-ttu-id="58c46-124">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="58c46-124">-Force</span></span>
<span data-ttu-id="58c46-125">Gibt an, dass dieses Cmdlet einen vorhandenen Hub ersetzt, ohne Sie zur Bestätigung auffordern zu müssen.</span><span class="sxs-lookup"><span data-stu-id="58c46-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="58c46-126">-Name</span><span class="sxs-lookup"><span data-stu-id="58c46-126">-Name</span></span>
<span data-ttu-id="58c46-127">Gibt den Namen des zu erstellenden Hubs an.</span><span class="sxs-lookup"><span data-stu-id="58c46-127">Specifies the name of the hub to create.</span></span>

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

### <span data-ttu-id="58c46-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58c46-128">-ResourceGroupName</span></span>
<span data-ttu-id="58c46-129">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="58c46-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="58c46-130">Dieses Cmdlet erstellt einen Hub, der zu der Gruppe gehört, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="58c46-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="58c46-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="58c46-131">-Confirm</span></span>
<span data-ttu-id="58c46-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="58c46-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58c46-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58c46-133">-WhatIf</span></span>
<span data-ttu-id="58c46-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="58c46-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58c46-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="58c46-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58c46-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c46-136">CommonParameters</span></span>
<span data-ttu-id="58c46-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58c46-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c46-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58c46-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c46-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="58c46-139">INPUTS</span></span>

### <span data-ttu-id="58c46-140">System.String</span><span class="sxs-lookup"><span data-stu-id="58c46-140">System.String</span></span>

### <span data-ttu-id="58c46-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="58c46-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="58c46-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="58c46-142">OUTPUTS</span></span>

### <span data-ttu-id="58c46-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span><span class="sxs-lookup"><span data-stu-id="58c46-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="58c46-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="58c46-144">NOTES</span></span>
* <span data-ttu-id="58c46-145">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="58c46-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="58c46-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="58c46-146">RELATED LINKS</span></span>

[<span data-ttu-id="58c46-147">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="58c46-147">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="58c46-148">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="58c46-148">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


