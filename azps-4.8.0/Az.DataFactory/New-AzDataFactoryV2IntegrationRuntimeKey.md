---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 07cb597f5ca3793e3eb8db3fe153fafaa94f3501
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173885"
---
# <span data-ttu-id="728a5-101">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="728a5-101">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="728a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="728a5-102">SYNOPSIS</span></span>
<span data-ttu-id="728a5-103">Generieren Sie den selbst gehosteten Integrationslauf Zeitschlüssel erneut.</span><span class="sxs-lookup"><span data-stu-id="728a5-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="728a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="728a5-104">SYNTAX</span></span>

### <span data-ttu-id="728a5-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="728a5-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="728a5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="728a5-106">ByResourceId</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="728a5-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="728a5-107">ByIntegrationRuntimeObject</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="728a5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="728a5-108">DESCRIPTION</span></span>
<span data-ttu-id="728a5-109">Das Cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** regeneriert den Integrationslauf Zeitschlüssel mit dem Schlüsselnamen, der durch den Parameter "keyname" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="728a5-109">The cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="728a5-110">Der vorherige Schlüssel ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="728a5-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="728a5-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="728a5-111">EXAMPLES</span></span>

### <span data-ttu-id="728a5-112">Beispiel 1: Generieren eines neuen Schlüssels für eine Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="728a5-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="728a5-113">Das Cmdlet generiert den Schlüssel "authKey2" für die Integrationslaufzeit mit dem Namen "Test-SelfHost-IR" neu.</span><span class="sxs-lookup"><span data-stu-id="728a5-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="728a5-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="728a5-114">PARAMETERS</span></span>

### <span data-ttu-id="728a5-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="728a5-115">-DataFactoryName</span></span>
<span data-ttu-id="728a5-116">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="728a5-116">The data factory name.</span></span>

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

### <span data-ttu-id="728a5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="728a5-117">-DefaultProfile</span></span>
<span data-ttu-id="728a5-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="728a5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="728a5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="728a5-119">-Force</span></span>
<span data-ttu-id="728a5-120">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="728a5-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="728a5-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="728a5-121">-InputObject</span></span>
<span data-ttu-id="728a5-122">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="728a5-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="728a5-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="728a5-123">-KeyName</span></span>
<span data-ttu-id="728a5-124">Der Authentifizierungsschlüssel Name der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="728a5-124">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="728a5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="728a5-125">-Name</span></span>
<span data-ttu-id="728a5-126">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="728a5-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="728a5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="728a5-127">-ResourceGroupName</span></span>
<span data-ttu-id="728a5-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="728a5-128">The resource group name.</span></span>

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

### <span data-ttu-id="728a5-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="728a5-129">-ResourceId</span></span>
<span data-ttu-id="728a5-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="728a5-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="728a5-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="728a5-131">-Confirm</span></span>
<span data-ttu-id="728a5-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="728a5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="728a5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="728a5-133">-WhatIf</span></span>
<span data-ttu-id="728a5-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="728a5-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="728a5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="728a5-135">CommonParameters</span></span>
<span data-ttu-id="728a5-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="728a5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="728a5-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="728a5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="728a5-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="728a5-138">INPUTS</span></span>

### <span data-ttu-id="728a5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="728a5-139">System.String</span></span>

### <span data-ttu-id="728a5-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="728a5-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="728a5-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="728a5-141">OUTPUTS</span></span>

### <span data-ttu-id="728a5-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="728a5-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="728a5-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="728a5-143">NOTES</span></span>

## <span data-ttu-id="728a5-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="728a5-144">RELATED LINKS</span></span>

[<span data-ttu-id="728a5-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="728a5-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
