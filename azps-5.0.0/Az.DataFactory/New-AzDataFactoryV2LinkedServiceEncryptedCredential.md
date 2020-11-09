---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 0ff9ef1337a1f2a5f0503c59dc4e6240d3c959b4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298402"
---
# <span data-ttu-id="6e935-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="6e935-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="6e935-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e935-102">SYNOPSIS</span></span>
<span data-ttu-id="6e935-103">Verschlüsseln von Anmeldeinformationen im verknüpften Dienst mit der angegebenen Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="6e935-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="6e935-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e935-104">SYNTAX</span></span>

### <span data-ttu-id="6e935-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6e935-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e935-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6e935-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e935-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e935-107">DESCRIPTION</span></span>
<span data-ttu-id="6e935-108">Das New-AzDataFactoryV2LinkedServiceEncryptedCredential-Cmdlet verschlüsseln Anmeldeinformationen im verknüpften Dienst mit der angegebenen Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="6e935-108">The New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="6e935-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e935-109">EXAMPLES</span></span>

### <span data-ttu-id="6e935-110">Beispiel 1: Verschlüsseln von Anmeldeinformationen in einem verknüpften Dienst</span><span class="sxs-lookup"><span data-stu-id="6e935-110">Example 1: Encrypt credentials in a linked service</span></span>

<span data-ttu-id="6e935-111">Mit diesem Befehl werden Anmeldeinformationen in Datei C:\samples\WikiSample\TaxiDemo1.jsmit der Integrationslaufzeit mit dem Namen Test-SelfHost-IR verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="6e935-111">This command encrypts credential in file C:\samples\WikiSample\TaxiDemo1.json with the integration runtime named test-selfhost-ir.</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzDataFactoryV2LinkedServiceEncryptedCredential -DataFactoryName WikiADF -DefinitionFile 'C:\samples\WikiSample\TaxiDemo1.json' -IntegrationRuntimeName 'test-selfhost-ir' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="6e935-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e935-112">PARAMETERS</span></span>

### <span data-ttu-id="6e935-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6e935-113">-DataFactory</span></span>
<span data-ttu-id="6e935-114">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6e935-114">The data factory object.</span></span>

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

### <span data-ttu-id="6e935-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="6e935-115">-DataFactoryName</span></span>
<span data-ttu-id="6e935-116">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="6e935-116">The data factory name.</span></span>

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

### <span data-ttu-id="6e935-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e935-117">-DefaultProfile</span></span>
<span data-ttu-id="6e935-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6e935-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e935-119">-Definitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="6e935-119">-DefinitionFile</span></span>
<span data-ttu-id="6e935-120">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="6e935-120">The JSON file path.</span></span>

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

### <span data-ttu-id="6e935-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6e935-121">-Force</span></span>
<span data-ttu-id="6e935-122">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="6e935-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6e935-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="6e935-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="6e935-124">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="6e935-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="6e935-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e935-125">-ResourceGroupName</span></span>
<span data-ttu-id="6e935-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6e935-126">The resource group name.</span></span>

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

### <span data-ttu-id="6e935-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6e935-127">-Confirm</span></span>
<span data-ttu-id="6e935-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6e935-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e935-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e935-129">-WhatIf</span></span>
<span data-ttu-id="6e935-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6e935-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="6e935-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e935-131">CommonParameters</span></span>
<span data-ttu-id="6e935-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e935-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e935-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e935-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e935-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e935-134">INPUTS</span></span>

### <span data-ttu-id="6e935-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6e935-135">System.String</span></span>

### <span data-ttu-id="6e935-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6e935-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="6e935-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e935-137">OUTPUTS</span></span>

### <span data-ttu-id="6e935-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6e935-138">System.String</span></span>

## <span data-ttu-id="6e935-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e935-139">NOTES</span></span>

## <span data-ttu-id="6e935-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e935-140">RELATED LINKS</span></span>
