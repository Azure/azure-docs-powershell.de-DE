---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 8571e210a39bc1d617b391eb4cf71aa45a34d69c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820380"
---
# <span data-ttu-id="fdafb-101">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="fdafb-101">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="fdafb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fdafb-102">SYNOPSIS</span></span>
<span data-ttu-id="fdafb-103">Generieren Sie den selbst gehosteten Integrationslauf Zeitschlüssel erneut.</span><span class="sxs-lookup"><span data-stu-id="fdafb-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="fdafb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdafb-104">SYNTAX</span></span>

### <span data-ttu-id="fdafb-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fdafb-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdafb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fdafb-106">ByResourceId</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdafb-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="fdafb-107">ByIntegrationRuntimeObject</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdafb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fdafb-108">DESCRIPTION</span></span>
<span data-ttu-id="fdafb-109">Das Cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** regeneriert den Integrationslauf Zeitschlüssel mit dem Schlüsselnamen, der durch den Parameter "keyname" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fdafb-109">The cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="fdafb-110">Der vorherige Schlüssel ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="fdafb-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="fdafb-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdafb-111">EXAMPLES</span></span>

### <span data-ttu-id="fdafb-112">Beispiel 1: Generieren eines neuen Schlüssels für eine Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="fdafb-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="fdafb-113">Das Cmdlet generiert den Schlüssel "authKey2" für die Integrationslaufzeit mit dem Namen "Test-SelfHost-IR" neu.</span><span class="sxs-lookup"><span data-stu-id="fdafb-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="fdafb-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdafb-114">PARAMETERS</span></span>

### <span data-ttu-id="fdafb-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="fdafb-115">-DataFactoryName</span></span>
<span data-ttu-id="fdafb-116">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="fdafb-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdafb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdafb-117">-DefaultProfile</span></span>
<span data-ttu-id="fdafb-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fdafb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdafb-119">-Force</span><span class="sxs-lookup"><span data-stu-id="fdafb-119">-Force</span></span>
<span data-ttu-id="fdafb-120">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="fdafb-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="fdafb-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fdafb-121">-InputObject</span></span>
<span data-ttu-id="fdafb-122">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="fdafb-122">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdafb-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="fdafb-123">-KeyName</span></span>
<span data-ttu-id="fdafb-124">Der Authentifizierungsschlüssel Name der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="fdafb-124">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdafb-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fdafb-125">-Name</span></span>
<span data-ttu-id="fdafb-126">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="fdafb-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdafb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdafb-127">-ResourceGroupName</span></span>
<span data-ttu-id="fdafb-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fdafb-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdafb-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fdafb-129">-ResourceId</span></span>
<span data-ttu-id="fdafb-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="fdafb-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdafb-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fdafb-131">-Confirm</span></span>
<span data-ttu-id="fdafb-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fdafb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdafb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdafb-133">-WhatIf</span></span>
<span data-ttu-id="fdafb-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fdafb-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="fdafb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdafb-135">CommonParameters</span></span>
<span data-ttu-id="fdafb-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdafb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdafb-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdafb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdafb-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fdafb-138">INPUTS</span></span>

### <span data-ttu-id="fdafb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fdafb-139">System.String</span></span>

### <span data-ttu-id="fdafb-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fdafb-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="fdafb-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fdafb-141">OUTPUTS</span></span>

### <span data-ttu-id="fdafb-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="fdafb-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="fdafb-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="fdafb-143">NOTES</span></span>

## <span data-ttu-id="fdafb-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fdafb-144">RELATED LINKS</span></span>

[<span data-ttu-id="fdafb-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="fdafb-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
