---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 9960a34d19c4016461ddfc53a37f83d3e73e7526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664278"
---
# <span data-ttu-id="d6ec1-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="d6ec1-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="d6ec1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d6ec1-102">SYNOPSIS</span></span>
<span data-ttu-id="d6ec1-103">Verschlüsseln von Anmeldeinformationen im verknüpften Dienst mit der angegebenen Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6ec1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6ec1-104">SYNTAX</span></span>

### <span data-ttu-id="d6ec1-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d6ec1-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d6ec1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d6ec1-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="d6ec1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6ec1-107">DESCRIPTION</span></span>
<span data-ttu-id="d6ec1-108">Das New-AzureRmDataFactoryV2LinkedServiceEncryptCredential-Cmdlet verschlüsseln Anmeldeinformationen im verknüpften Dienst mit der angegebenen Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="d6ec1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6ec1-109">EXAMPLES</span></span>

### <span data-ttu-id="d6ec1-110">Beispiel 1: Verschlüsseln von creadentials in einem verknüpften Dienst</span><span class="sxs-lookup"><span data-stu-id="d6ec1-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="d6ec1-111">Dieser Befehl verschlüsselt Anmeldeinformationen in Datei D:\sql.jsmit der Integrationslaufzeit mit dem Namen myIR.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="d6ec1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6ec1-112">PARAMETERS</span></span>

### <span data-ttu-id="d6ec1-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d6ec1-113">-DataFactory</span></span>
<span data-ttu-id="d6ec1-114">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-114">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ec1-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d6ec1-115">-DataFactoryName</span></span>
<span data-ttu-id="d6ec1-116">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-116">The data factory name.</span></span>

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

### <span data-ttu-id="d6ec1-117">-Definitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-117">-DefinitionFile</span></span>
<span data-ttu-id="d6ec1-118">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-118">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ec1-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d6ec1-119">-Force</span></span>
<span data-ttu-id="d6ec1-120">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d6ec1-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="d6ec1-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="d6ec1-122">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-122">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ec1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6ec1-123">-ResourceGroupName</span></span>
<span data-ttu-id="d6ec1-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-124">The resource group name.</span></span>

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

### <span data-ttu-id="d6ec1-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d6ec1-125">-Confirm</span></span>
<span data-ttu-id="d6ec1-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6ec1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6ec1-127">-WhatIf</span></span>
<span data-ttu-id="d6ec1-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d6ec1-128">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="d6ec1-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d6ec1-129">INPUTS</span></span>

### <span data-ttu-id="d6ec1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d6ec1-130">System.String</span></span>
<span data-ttu-id="d6ec1-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d6ec1-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="d6ec1-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d6ec1-132">OUTPUTS</span></span>

### <span data-ttu-id="d6ec1-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d6ec1-133">System.String</span></span>


## <span data-ttu-id="d6ec1-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="d6ec1-134">NOTES</span></span>

## <span data-ttu-id="d6ec1-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d6ec1-135">RELATED LINKS</span></span>

