---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: f98a5efeece2eb1e78479c3f76de62db495c6e43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930779"
---
# <span data-ttu-id="2646f-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="2646f-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="2646f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2646f-102">SYNOPSIS</span></span>
<span data-ttu-id="2646f-103">Fügen Sie dem Cluster eine oder mehrere Service Fabric-Einstellungen hinzu, oder aktualisieren Sie sie.</span><span class="sxs-lookup"><span data-stu-id="2646f-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="2646f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2646f-104">SYNTAX</span></span>

### <span data-ttu-id="2646f-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="2646f-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2646f-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="2646f-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2646f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2646f-107">DESCRIPTION</span></span>
<span data-ttu-id="2646f-108">Verwenden **Sie Set-AzServiceFabricSetting,** um Service Fabric-Einstellungen in einem Cluster hinzuzufügen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2646f-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="2646f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2646f-109">EXAMPLES</span></span>

### <span data-ttu-id="2646f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2646f-110">Example 1</span></span>
```
Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="2646f-111">Mit diesem Befehl wird "MaxFileOperationTimeout" unter dem Abschnitt "NamingService" auf den Wert "5000" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2646f-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>


### <span data-ttu-id="2646f-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2646f-112">Example 2</span></span>
```
$fabricSettings = @(
    @{ 
        "name" = "NamingService";
        "parameters" =  [System.Collections.Generic.List[Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsParameterDescription]]@(
            @{ "Name" = "MaxFileOperationTimeout"; "Value" = "5000"  };
            @{ "Name" = "MaxOperationTimeout"; "Value" = "1200"  })
    },
    @{ 
        "name" = "Hosting";
        "parameters" =  [System.Collections.Generic.List[Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsParameterDescription]]@(
            @{ "Name" = "ActivationMaxFailureCount"; "Value" = "11"  })
    })

Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SettingsSectionDescription $fabricSettings -Verbose
```

<span data-ttu-id="2646f-113">Dieser Befehl löst ein Upgrade zum Festlegen mehrerer Fabriceinstellungen mit dem Parameter SettingsSectionDescription aus.</span><span class="sxs-lookup"><span data-stu-id="2646f-113">This command will trigger an upgrade to set multiple fabric setting using SettingsSectionDescription parameter.</span></span>

## <span data-ttu-id="2646f-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2646f-114">PARAMETERS</span></span>

### <span data-ttu-id="2646f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2646f-115">-DefaultProfile</span></span>
<span data-ttu-id="2646f-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2646f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2646f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2646f-117">-Name</span></span>
<span data-ttu-id="2646f-118">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="2646f-118">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2646f-119">-Parameter</span><span class="sxs-lookup"><span data-stu-id="2646f-119">-Parameter</span></span>
<span data-ttu-id="2646f-120">Parametername der Fabriceinstellung</span><span class="sxs-lookup"><span data-stu-id="2646f-120">Parameter name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2646f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2646f-121">-ResourceGroupName</span></span>
<span data-ttu-id="2646f-122">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2646f-122">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2646f-123">-Section</span><span class="sxs-lookup"><span data-stu-id="2646f-123">-Section</span></span>
<span data-ttu-id="2646f-124">Abschnittsname der Fabriceinstellung</span><span class="sxs-lookup"><span data-stu-id="2646f-124">Section name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2646f-125">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="2646f-125">-SettingsSectionDescription</span></span>
<span data-ttu-id="2646f-126">Eine Matrix von Fabriceinstellungen</span><span class="sxs-lookup"><span data-stu-id="2646f-126">An array of fabric settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2646f-127">-Wert</span><span class="sxs-lookup"><span data-stu-id="2646f-127">-Value</span></span>
<span data-ttu-id="2646f-128">Parameterwert der Fabriceinstellung</span><span class="sxs-lookup"><span data-stu-id="2646f-128">Parameter value of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2646f-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2646f-129">-Confirm</span></span>
<span data-ttu-id="2646f-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2646f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2646f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2646f-131">-WhatIf</span></span>
<span data-ttu-id="2646f-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2646f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2646f-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2646f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2646f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2646f-134">CommonParameters</span></span>
<span data-ttu-id="2646f-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2646f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2646f-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2646f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2646f-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2646f-137">INPUTS</span></span>

### <span data-ttu-id="2646f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2646f-138">System.String</span></span>

### <span data-ttu-id="2646f-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span><span class="sxs-lookup"><span data-stu-id="2646f-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="2646f-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2646f-140">OUTPUTS</span></span>

### <span data-ttu-id="2646f-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="2646f-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="2646f-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2646f-142">NOTES</span></span>

## <span data-ttu-id="2646f-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2646f-143">RELATED LINKS</span></span>
