---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 166bae99bebbc5a1b1c25ffc79faa3a1f7254bbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662432"
---
# <span data-ttu-id="f1623-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="f1623-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="f1623-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1623-102">SYNOPSIS</span></span>
<span data-ttu-id="f1623-103">Generieren Sie den selbst gehosteten Integrationslauf Zeitschlüssel erneut.</span><span class="sxs-lookup"><span data-stu-id="f1623-103">Regenerate self-hosted integration runtime key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1623-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1623-104">SYNTAX</span></span>

### <span data-ttu-id="f1623-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1623-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f1623-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f1623-106">ByResourceId</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String> [-WhatIf]
 [-Confirm]
```

### <span data-ttu-id="f1623-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="f1623-107">ByIntegrationRuntimeObject</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f1623-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1623-108">DESCRIPTION</span></span>
<span data-ttu-id="f1623-109">Das Cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regeneriert den Integrationslauf Zeitschlüssel mit dem Schlüsselnamen, der durch den Parameter "keyname" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f1623-109">The cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="f1623-110">Der vorherige Schlüssel ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f1623-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="f1623-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1623-111">EXAMPLES</span></span>

### <span data-ttu-id="f1623-112">Beispiel 1: Generieren eines neuen Schlüssels für eine Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="f1623-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="f1623-113">Das Cmdlet generiert den Schlüssel "authKey2" für die Integrationslaufzeit mit dem Namen "Test-SelfHost-IR" neu.</span><span class="sxs-lookup"><span data-stu-id="f1623-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="f1623-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1623-114">PARAMETERS</span></span>

### <span data-ttu-id="f1623-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1623-115">-Confirm</span></span>
<span data-ttu-id="f1623-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1623-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1623-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="f1623-117">-DataFactoryName</span></span>
<span data-ttu-id="f1623-118">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="f1623-118">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1623-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f1623-119">-Force</span></span>
<span data-ttu-id="f1623-120">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="f1623-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f1623-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f1623-121">-InputObject</span></span>
<span data-ttu-id="f1623-122">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="f1623-122">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1623-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="f1623-123">-KeyName</span></span>
<span data-ttu-id="f1623-124">Der Authentifizierungsschlüssel Name der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="f1623-124">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1623-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f1623-125">-Name</span></span>
<span data-ttu-id="f1623-126">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="f1623-126">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1623-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1623-127">-ResourceGroupName</span></span>
<span data-ttu-id="f1623-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f1623-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1623-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f1623-129">-ResourceId</span></span>
<span data-ttu-id="f1623-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f1623-130">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1623-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1623-131">-WhatIf</span></span>
<span data-ttu-id="f1623-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1623-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="f1623-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1623-133">INPUTS</span></span>

### <span data-ttu-id="f1623-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f1623-134">System.String</span></span>
<span data-ttu-id="f1623-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f1623-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="f1623-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1623-136">OUTPUTS</span></span>

### <span data-ttu-id="f1623-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="f1623-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>


## <span data-ttu-id="f1623-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1623-138">NOTES</span></span>

## <span data-ttu-id="f1623-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1623-139">RELATED LINKS</span></span>
[<span data-ttu-id="f1623-140">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="f1623-140">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
