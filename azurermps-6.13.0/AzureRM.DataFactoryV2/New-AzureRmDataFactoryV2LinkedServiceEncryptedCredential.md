---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 765bd2c75a377204ab4566f47d0498deaf127953
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476149"
---
# <span data-ttu-id="9b28c-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="9b28c-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="9b28c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9b28c-102">SYNOPSIS</span></span>
<span data-ttu-id="9b28c-103">Verschlüsseln von Anmeldeinformationen im verknüpften Dienst mit der angegebenen Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="9b28c-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b28c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b28c-104">SYNTAX</span></span>

### <span data-ttu-id="9b28c-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9b28c-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b28c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9b28c-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b28c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b28c-107">DESCRIPTION</span></span>
<span data-ttu-id="9b28c-108">Das New-AzureRmDataFactoryV2LinkedServiceEncryptCredential-Cmdlet verschlüsseln Anmeldeinformationen im verknüpften Dienst mit der angegebenen Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="9b28c-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="9b28c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b28c-109">EXAMPLES</span></span>

### <span data-ttu-id="9b28c-110">Beispiel 1: Verschlüsseln von creadentials in einem verknüpften Dienst</span><span class="sxs-lookup"><span data-stu-id="9b28c-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="9b28c-111">Dieser Befehl verschlüsselt Anmeldeinformationen in Datei D:\sql.jsmit der Integrationslaufzeit mit dem Namen myIR.</span><span class="sxs-lookup"><span data-stu-id="9b28c-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="9b28c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b28c-112">PARAMETERS</span></span>

### <span data-ttu-id="9b28c-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9b28c-113">-DataFactory</span></span>
<span data-ttu-id="9b28c-114">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9b28c-114">The data factory object.</span></span>

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

### <span data-ttu-id="9b28c-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="9b28c-115">-DataFactoryName</span></span>
<span data-ttu-id="9b28c-116">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="9b28c-116">The data factory name.</span></span>

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

### <span data-ttu-id="9b28c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b28c-117">-DefaultProfile</span></span>
<span data-ttu-id="9b28c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9b28c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b28c-119">-Definitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="9b28c-119">-DefinitionFile</span></span>
<span data-ttu-id="9b28c-120">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="9b28c-120">The JSON file path.</span></span>

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

### <span data-ttu-id="9b28c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9b28c-121">-Force</span></span>
<span data-ttu-id="9b28c-122">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="9b28c-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="9b28c-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="9b28c-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="9b28c-124">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="9b28c-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="9b28c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b28c-125">-ResourceGroupName</span></span>
<span data-ttu-id="9b28c-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9b28c-126">The resource group name.</span></span>

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

### <span data-ttu-id="9b28c-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9b28c-127">-Confirm</span></span>
<span data-ttu-id="9b28c-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9b28c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b28c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b28c-129">-WhatIf</span></span>
<span data-ttu-id="9b28c-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b28c-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="9b28c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b28c-131">CommonParameters</span></span>
<span data-ttu-id="9b28c-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b28c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b28c-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b28c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b28c-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9b28c-134">INPUTS</span></span>

### <span data-ttu-id="9b28c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9b28c-135">System.String</span></span>

### <span data-ttu-id="9b28c-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9b28c-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="9b28c-137">Parameter: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9b28c-137">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="9b28c-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9b28c-138">OUTPUTS</span></span>

### <span data-ttu-id="9b28c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9b28c-139">System.String</span></span>

## <span data-ttu-id="9b28c-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="9b28c-140">NOTES</span></span>

## <span data-ttu-id="9b28c-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9b28c-141">RELATED LINKS</span></span>
