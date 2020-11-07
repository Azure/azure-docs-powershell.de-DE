---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 3face29daf5c6da80e5d6b277850c6639efe96dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662909"
---
# <span data-ttu-id="08545-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="08545-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="08545-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08545-102">SYNOPSIS</span></span>
<span data-ttu-id="08545-103">Verschlüsseln von Anmeldeinformationen im verknüpften Dienst mit der angegebenen Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="08545-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08545-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08545-104">SYNTAX</span></span>

### <span data-ttu-id="08545-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="08545-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08545-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="08545-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08545-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08545-107">DESCRIPTION</span></span>
<span data-ttu-id="08545-108">Das New-AzureRmDataFactoryV2LinkedServiceEncryptCredential-Cmdlet verschlüsseln Anmeldeinformationen im verknüpften Dienst mit der angegebenen Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="08545-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="08545-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08545-109">EXAMPLES</span></span>

### <span data-ttu-id="08545-110">Beispiel 1: Verschlüsseln von creadentials in einem verknüpften Dienst</span><span class="sxs-lookup"><span data-stu-id="08545-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="08545-111">Dieser Befehl verschlüsselt Anmeldeinformationen in Datei D:\sql.jsmit der Integrationslaufzeit mit dem Namen myIR.</span><span class="sxs-lookup"><span data-stu-id="08545-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="08545-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="08545-112">PARAMETERS</span></span>

### <span data-ttu-id="08545-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="08545-113">-DataFactory</span></span>
<span data-ttu-id="08545-114">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="08545-114">The data factory object.</span></span>

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

### <span data-ttu-id="08545-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="08545-115">-DataFactoryName</span></span>
<span data-ttu-id="08545-116">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="08545-116">The data factory name.</span></span>

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

### <span data-ttu-id="08545-117">-Definitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="08545-117">-DefinitionFile</span></span>
<span data-ttu-id="08545-118">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="08545-118">The JSON file path.</span></span>

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

### <span data-ttu-id="08545-119">-Force</span><span class="sxs-lookup"><span data-stu-id="08545-119">-Force</span></span>
<span data-ttu-id="08545-120">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="08545-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="08545-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="08545-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="08545-122">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="08545-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="08545-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08545-123">-ResourceGroupName</span></span>
<span data-ttu-id="08545-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="08545-124">The resource group name.</span></span>

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

### <span data-ttu-id="08545-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="08545-125">-Confirm</span></span>
<span data-ttu-id="08545-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08545-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08545-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08545-127">-WhatIf</span></span>
<span data-ttu-id="08545-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08545-128">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="08545-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08545-129">-DefaultProfile</span></span>
<span data-ttu-id="08545-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="08545-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08545-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08545-131">CommonParameters</span></span>
<span data-ttu-id="08545-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08545-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08545-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08545-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08545-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08545-134">INPUTS</span></span>

### <span data-ttu-id="08545-135">System. String</span><span class="sxs-lookup"><span data-stu-id="08545-135">System.String</span></span>
<span data-ttu-id="08545-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="08545-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="08545-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08545-137">OUTPUTS</span></span>

### <span data-ttu-id="08545-138">System. String</span><span class="sxs-lookup"><span data-stu-id="08545-138">System.String</span></span>

## <span data-ttu-id="08545-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="08545-139">NOTES</span></span>

## <span data-ttu-id="08545-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08545-140">RELATED LINKS</span></span>

