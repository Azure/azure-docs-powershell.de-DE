---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: 871f3ba59fb84cea10200a7983fe7ee80b68918e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158369"
---
# <span data-ttu-id="594bf-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="594bf-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="594bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="594bf-102">SYNOPSIS</span></span>
<span data-ttu-id="594bf-103">Fügen Sie dem Cluster eine oder mehrere Service Fabric-Einstellungen hinzu, oder aktualisieren Sie sie.</span><span class="sxs-lookup"><span data-stu-id="594bf-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="594bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="594bf-104">SYNTAX</span></span>

### <span data-ttu-id="594bf-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="594bf-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="594bf-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="594bf-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="594bf-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="594bf-107">DESCRIPTION</span></span>
<span data-ttu-id="594bf-108">Verwenden **Sie Set-AzServiceFabricSetting zum** Hinzufügen oder Aktualisieren von Service Fabric-Einstellungen in einem Cluster.</span><span class="sxs-lookup"><span data-stu-id="594bf-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="594bf-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="594bf-109">EXAMPLES</span></span>

### <span data-ttu-id="594bf-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="594bf-110">Example 1</span></span>
```
Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="594bf-111">Mit diesem Befehl wird "MaxFileOperationTimeout" unter dem Abschnitt "NamingService" auf den Wert "5000" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="594bf-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>


### <span data-ttu-id="594bf-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="594bf-112">Example 2</span></span>
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

<span data-ttu-id="594bf-113">This command will trigger an upgrade to set multiple fabric setting using SettingsSectionDescription parameter.</span><span class="sxs-lookup"><span data-stu-id="594bf-113">This command will trigger an upgrade to set multiple fabric setting using SettingsSectionDescription parameter.</span></span>

## <span data-ttu-id="594bf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="594bf-114">PARAMETERS</span></span>

### <span data-ttu-id="594bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="594bf-115">-DefaultProfile</span></span>
<span data-ttu-id="594bf-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="594bf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="594bf-117">-Name</span><span class="sxs-lookup"><span data-stu-id="594bf-117">-Name</span></span>
<span data-ttu-id="594bf-118">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="594bf-118">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="594bf-119">-Parameter</span><span class="sxs-lookup"><span data-stu-id="594bf-119">-Parameter</span></span>
<span data-ttu-id="594bf-120">Parametername der Fabriceinstellung</span><span class="sxs-lookup"><span data-stu-id="594bf-120">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="594bf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="594bf-121">-ResourceGroupName</span></span>
<span data-ttu-id="594bf-122">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="594bf-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="594bf-123">-Section</span><span class="sxs-lookup"><span data-stu-id="594bf-123">-Section</span></span>
<span data-ttu-id="594bf-124">Section name of the fabric setting</span><span class="sxs-lookup"><span data-stu-id="594bf-124">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="594bf-125">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="594bf-125">-SettingsSectionDescription</span></span>
<span data-ttu-id="594bf-126">An array of fabric settings</span><span class="sxs-lookup"><span data-stu-id="594bf-126">An array of fabric settings</span></span>

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

### <span data-ttu-id="594bf-127">-Value</span><span class="sxs-lookup"><span data-stu-id="594bf-127">-Value</span></span>
<span data-ttu-id="594bf-128">Parameter value of the fabric setting</span><span class="sxs-lookup"><span data-stu-id="594bf-128">Parameter value of the fabric setting</span></span>

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

### <span data-ttu-id="594bf-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="594bf-129">-Confirm</span></span>
<span data-ttu-id="594bf-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="594bf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="594bf-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="594bf-131">-WhatIf</span></span>
<span data-ttu-id="594bf-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="594bf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="594bf-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="594bf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="594bf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="594bf-134">CommonParameters</span></span>
<span data-ttu-id="594bf-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="594bf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="594bf-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="594bf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="594bf-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="594bf-137">INPUTS</span></span>

### <span data-ttu-id="594bf-138">System.String</span><span class="sxs-lookup"><span data-stu-id="594bf-138">System.String</span></span>

### <span data-ttu-id="594bf-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span><span class="sxs-lookup"><span data-stu-id="594bf-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="594bf-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="594bf-140">OUTPUTS</span></span>

### <span data-ttu-id="594bf-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="594bf-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="594bf-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="594bf-142">NOTES</span></span>

## <span data-ttu-id="594bf-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="594bf-143">RELATED LINKS</span></span>
