---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: becbcd3e7bbc0a86a2b092921fd5060dd56e927b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665083"
---
# <span data-ttu-id="3b366-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="3b366-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="3b366-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3b366-102">SYNOPSIS</span></span>
<span data-ttu-id="3b366-103">Generieren Sie den selbst gehosteten Integrationslauf Zeitschlüssel erneut.</span><span class="sxs-lookup"><span data-stu-id="3b366-103">Regenerate self-hosted integration runtime key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b366-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b366-104">SYNTAX</span></span>

### <span data-ttu-id="3b366-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3b366-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b366-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3b366-106">ByResourceId</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b366-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="3b366-107">ByIntegrationRuntimeObject</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b366-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b366-108">DESCRIPTION</span></span>
<span data-ttu-id="3b366-109">Das Cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regeneriert den Integrationslauf Zeitschlüssel mit dem Schlüsselnamen, der durch den Parameter "keyname" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3b366-109">The cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="3b366-110">Der vorherige Schlüssel ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="3b366-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="3b366-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b366-111">EXAMPLES</span></span>

### <span data-ttu-id="3b366-112">Beispiel 1: Generieren eines neuen Schlüssels für eine Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="3b366-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="3b366-113">Das Cmdlet generiert den Schlüssel "authKey2" für die Integrationslaufzeit mit dem Namen "Test-SelfHost-IR" neu.</span><span class="sxs-lookup"><span data-stu-id="3b366-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="3b366-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b366-114">PARAMETERS</span></span>

### <span data-ttu-id="3b366-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3b366-115">-Confirm</span></span>
<span data-ttu-id="3b366-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b366-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b366-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="3b366-117">-DataFactoryName</span></span>
<span data-ttu-id="3b366-118">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="3b366-118">The data factory name.</span></span>

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

### <span data-ttu-id="3b366-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3b366-119">-Force</span></span>
<span data-ttu-id="3b366-120">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="3b366-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3b366-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3b366-121">-InputObject</span></span>
<span data-ttu-id="3b366-122">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="3b366-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="3b366-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="3b366-123">-KeyName</span></span>
<span data-ttu-id="3b366-124">Der Authentifizierungsschlüssel Name der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="3b366-124">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="3b366-125">-Name</span><span class="sxs-lookup"><span data-stu-id="3b366-125">-Name</span></span>
<span data-ttu-id="3b366-126">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="3b366-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="3b366-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b366-127">-ResourceGroupName</span></span>
<span data-ttu-id="3b366-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3b366-128">The resource group name.</span></span>

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

### <span data-ttu-id="3b366-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3b366-129">-ResourceId</span></span>
<span data-ttu-id="3b366-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="3b366-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3b366-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b366-131">-WhatIf</span></span>
<span data-ttu-id="3b366-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b366-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3b366-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b366-133">-DefaultProfile</span></span>
<span data-ttu-id="3b366-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3b366-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b366-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b366-135">CommonParameters</span></span>
<span data-ttu-id="3b366-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b366-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b366-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b366-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b366-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3b366-138">INPUTS</span></span>

### <span data-ttu-id="3b366-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3b366-139">System.String</span></span>
<span data-ttu-id="3b366-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3b366-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3b366-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3b366-141">OUTPUTS</span></span>

### <span data-ttu-id="3b366-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="3b366-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="3b366-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b366-143">NOTES</span></span>

## <span data-ttu-id="3b366-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3b366-144">RELATED LINKS</span></span>

[<span data-ttu-id="3b366-145">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="3b366-145">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
