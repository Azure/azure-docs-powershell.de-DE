---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: a3bccd635c5bb2a91cb0b8ea9bc09f93070d447d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480382"
---
# <span data-ttu-id="d5232-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="d5232-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="d5232-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d5232-102">SYNOPSIS</span></span>
<span data-ttu-id="d5232-103">Generieren Sie den selbst gehosteten Integrationslauf Zeitschlüssel erneut.</span><span class="sxs-lookup"><span data-stu-id="d5232-103">Regenerate self-hosted integration runtime key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5232-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5232-104">SYNTAX</span></span>

### <span data-ttu-id="d5232-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d5232-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5232-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d5232-106">ByResourceId</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5232-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="d5232-107">ByIntegrationRuntimeObject</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5232-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5232-108">DESCRIPTION</span></span>
<span data-ttu-id="d5232-109">Das Cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regeneriert den Integrationslauf Zeitschlüssel mit dem Schlüsselnamen, der durch den Parameter "keyname" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d5232-109">The cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="d5232-110">Der vorherige Schlüssel ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d5232-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="d5232-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5232-111">EXAMPLES</span></span>

### <span data-ttu-id="d5232-112">Beispiel 1: Generieren eines neuen Schlüssels für eine Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="d5232-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="d5232-113">Das Cmdlet generiert den Schlüssel "authKey2" für die Integrationslaufzeit mit dem Namen "Test-SelfHost-IR" neu.</span><span class="sxs-lookup"><span data-stu-id="d5232-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="d5232-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5232-114">PARAMETERS</span></span>

### <span data-ttu-id="d5232-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d5232-115">-DataFactoryName</span></span>
<span data-ttu-id="d5232-116">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="d5232-116">The data factory name.</span></span>

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

### <span data-ttu-id="d5232-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5232-117">-DefaultProfile</span></span>
<span data-ttu-id="d5232-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d5232-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5232-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d5232-119">-Force</span></span>
<span data-ttu-id="d5232-120">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="d5232-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d5232-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d5232-121">-InputObject</span></span>
<span data-ttu-id="d5232-122">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="d5232-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="d5232-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d5232-123">-KeyName</span></span>
<span data-ttu-id="d5232-124">Der Authentifizierungsschlüssel Name der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="d5232-124">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="d5232-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d5232-125">-Name</span></span>
<span data-ttu-id="d5232-126">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="d5232-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="d5232-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5232-127">-ResourceGroupName</span></span>
<span data-ttu-id="d5232-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d5232-128">The resource group name.</span></span>

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

### <span data-ttu-id="d5232-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d5232-129">-ResourceId</span></span>
<span data-ttu-id="d5232-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="d5232-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d5232-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d5232-131">-Confirm</span></span>
<span data-ttu-id="d5232-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5232-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5232-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5232-133">-WhatIf</span></span>
<span data-ttu-id="d5232-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5232-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d5232-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5232-135">CommonParameters</span></span>
<span data-ttu-id="d5232-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5232-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5232-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5232-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5232-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d5232-138">INPUTS</span></span>

### <span data-ttu-id="d5232-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d5232-139">System.String</span></span>

### <span data-ttu-id="d5232-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d5232-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="d5232-141">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d5232-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d5232-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d5232-142">OUTPUTS</span></span>

### <span data-ttu-id="d5232-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="d5232-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="d5232-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="d5232-144">NOTES</span></span>

## <span data-ttu-id="d5232-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d5232-145">RELATED LINKS</span></span>

[<span data-ttu-id="d5232-146">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="d5232-146">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
