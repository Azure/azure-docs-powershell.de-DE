---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: a99f7fbb1383d685a53cc11f9dd81f6f306ed633
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470562"
---
# <span data-ttu-id="1cb1e-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="1cb1e-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="1cb1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cb1e-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb1e-103">Verschlüsseln Sie die Anmeldeinformationen im verknüpften Dienst mit der angegebenen Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="1cb1e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1cb1e-104">SYNTAX</span></span>

### <span data-ttu-id="1cb1e-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1cb1e-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb1e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1cb1e-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cb1e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1cb1e-107">DESCRIPTION</span></span>
<span data-ttu-id="1cb1e-108">Das New-AzDataFactoryV2LinkedServiceEncryptedCredential die Anmeldeinformationen im verknüpften Dienst mit der angegebenen Integrationslaufzeit verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-108">The New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

<span data-ttu-id="1cb1e-109">Stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="1cb1e-109">Please ensure the following prerequisites are met:</span></span>
* <span data-ttu-id="1cb1e-110">**Die Remotezugriffsoption** ist für die selbst gehostete Integrationslaufzeit aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-110">**Remote access** option is enabled on the self-hosted integration runtime.</span></span>
* <span data-ttu-id="1cb1e-111">Zum Ausführen des Cmdlets wird Powershell 7.0 oder höher verwendet.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-111">Powershell 7.0 or higher is used to execute the cmdlet.</span></span>

## <span data-ttu-id="1cb1e-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1cb1e-112">EXAMPLES</span></span>

### <span data-ttu-id="1cb1e-113">Beispiel 1: Verschlüsseln von Anmeldeinformationen in einem verknüpften Dienst</span><span class="sxs-lookup"><span data-stu-id="1cb1e-113">Example 1: Encrypt credentials in a linked service</span></span>

<span data-ttu-id="1cb1e-114">Mit diesem Befehl werden die Anmeldeinformationen in C:\samples\WikiSample\TaxiDemo1.jsmit der Integrationslaufzeit namens "test-selfhost-ir" verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-114">This command encrypts credential in file C:\samples\WikiSample\TaxiDemo1.json with the integration runtime named test-selfhost-ir.</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzDataFactoryV2LinkedServiceEncryptedCredential -DataFactoryName WikiADF -DefinitionFile 'C:\samples\WikiSample\TaxiDemo1.json' -IntegrationRuntimeName 'test-selfhost-ir' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="1cb1e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cb1e-115">PARAMETERS</span></span>

### <span data-ttu-id="1cb1e-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1cb1e-116">-DataFactory</span></span>
<span data-ttu-id="1cb1e-117">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb1e-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1cb1e-118">-DataFactoryName</span></span>
<span data-ttu-id="1cb1e-119">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-119">The data factory name.</span></span>

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

### <span data-ttu-id="1cb1e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb1e-120">-DefaultProfile</span></span>
<span data-ttu-id="1cb1e-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cb1e-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="1cb1e-122">-DefinitionFile</span></span>
<span data-ttu-id="1cb1e-123">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-123">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb1e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="1cb1e-124">-Force</span></span>
<span data-ttu-id="1cb1e-125">Führt das Cmdlet ohne Bestätigungsaufforderung aus.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="1cb1e-126">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="1cb1e-126">-IntegrationRuntimeName</span></span>
<span data-ttu-id="1cb1e-127">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-127">The integration runtime name.</span></span>

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

### <span data-ttu-id="1cb1e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cb1e-128">-ResourceGroupName</span></span>
<span data-ttu-id="1cb1e-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-129">The resource group name.</span></span>

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

### <span data-ttu-id="1cb1e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cb1e-130">-Confirm</span></span>
<span data-ttu-id="1cb1e-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cb1e-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1cb1e-132">-WhatIf</span></span>
<span data-ttu-id="1cb1e-133">Zeigt, was geschieht, wenn das Cmdlet ausgeführt, aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="1cb1e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb1e-134">CommonParameters</span></span>
<span data-ttu-id="1cb1e-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cb1e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb1e-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cb1e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb1e-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1cb1e-137">INPUTS</span></span>

### <span data-ttu-id="1cb1e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1cb1e-138">System.String</span></span>

### <span data-ttu-id="1cb1e-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1cb1e-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="1cb1e-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1cb1e-140">OUTPUTS</span></span>

### <span data-ttu-id="1cb1e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="1cb1e-141">System.String</span></span>

## <span data-ttu-id="1cb1e-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1cb1e-142">NOTES</span></span>

## <span data-ttu-id="1cb1e-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1cb1e-143">RELATED LINKS</span></span>
