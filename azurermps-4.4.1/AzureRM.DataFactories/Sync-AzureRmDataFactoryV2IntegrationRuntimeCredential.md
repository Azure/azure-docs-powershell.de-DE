---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: e89f4c69996f5527c49db72f3185e5a126b348c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479853"
---
# <span data-ttu-id="3efe5-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="3efe5-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="3efe5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3efe5-102">SYNOPSIS</span></span>
<span data-ttu-id="3efe5-103">Synchronisiert Anmeldeinformationen zwischen Integrationslauf Zeit Knoten.</span><span class="sxs-lookup"><span data-stu-id="3efe5-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3efe5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3efe5-104">SYNTAX</span></span>

### <span data-ttu-id="3efe5-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3efe5-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3efe5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3efe5-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3efe5-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="3efe5-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3efe5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3efe5-108">DESCRIPTION</span></span>
<span data-ttu-id="3efe5-109">Das Cmdlet " **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** " synchronisiert lokale Anmeldeinformationen zwischen Integrationslauf Zeit Knoten, wodurch die Anmeldeinformationen in allen Knoten identisch sind.</span><span class="sxs-lookup"><span data-stu-id="3efe5-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="3efe5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3efe5-110">EXAMPLES</span></span>

### <span data-ttu-id="3efe5-111">Beispiel 1: Synchronisieren einer Integration Runtime-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="3efe5-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="3efe5-112">Mit dem Cmdlet werden die Anmeldeinformationen zwischen Integrationslauf Zeit Knoten synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="3efe5-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="3efe5-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3efe5-113">PARAMETERS</span></span>

### <span data-ttu-id="3efe5-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3efe5-114">-Confirm</span></span>
<span data-ttu-id="3efe5-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3efe5-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3efe5-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="3efe5-116">-DataFactoryName</span></span>
<span data-ttu-id="3efe5-117">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="3efe5-117">The data factory name.</span></span>

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

### <span data-ttu-id="3efe5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3efe5-118">-Force</span></span>
<span data-ttu-id="3efe5-119">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="3efe5-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3efe5-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3efe5-120">-InputObject</span></span>
<span data-ttu-id="3efe5-121">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="3efe5-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="3efe5-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="3efe5-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="3efe5-123">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="3efe5-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3efe5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3efe5-124">-ResourceGroupName</span></span>
<span data-ttu-id="3efe5-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3efe5-125">The resource group name.</span></span>

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

### <span data-ttu-id="3efe5-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3efe5-126">-ResourceId</span></span>
<span data-ttu-id="3efe5-127">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="3efe5-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3efe5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3efe5-128">-WhatIf</span></span>
<span data-ttu-id="3efe5-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3efe5-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3efe5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3efe5-130">-DefaultProfile</span></span>
<span data-ttu-id="3efe5-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3efe5-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3efe5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3efe5-132">CommonParameters</span></span>
<span data-ttu-id="3efe5-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3efe5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3efe5-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3efe5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3efe5-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3efe5-135">INPUTS</span></span>

### <span data-ttu-id="3efe5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3efe5-136">System.String</span></span>
<span data-ttu-id="3efe5-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3efe5-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3efe5-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3efe5-138">OUTPUTS</span></span>

### <span data-ttu-id="3efe5-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="3efe5-139">System.Object</span></span>

## <span data-ttu-id="3efe5-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="3efe5-140">NOTES</span></span>

## <span data-ttu-id="3efe5-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3efe5-141">RELATED LINKS</span></span>

