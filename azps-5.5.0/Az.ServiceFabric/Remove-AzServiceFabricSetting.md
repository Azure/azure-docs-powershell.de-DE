---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: db6d94b4aa2f6182abc114f11d1dba0b40ebbb93
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150668"
---
# <span data-ttu-id="d3a47-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="d3a47-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="d3a47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3a47-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a47-103">Remove one or multiple Service Fabric setting from the cluster.</span><span class="sxs-lookup"><span data-stu-id="d3a47-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="d3a47-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3a47-104">SYNTAX</span></span>

### <span data-ttu-id="d3a47-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="d3a47-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3a47-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="d3a47-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3a47-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3a47-107">DESCRIPTION</span></span>
<span data-ttu-id="d3a47-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span><span class="sxs-lookup"><span data-stu-id="d3a47-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="d3a47-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d3a47-109">EXAMPLES</span></span>

### <span data-ttu-id="d3a47-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d3a47-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="d3a47-111">Mit diesem Befehl werden die Einstellungen "MaxCursors" im Abschnitt "EseStore" entfernt.</span><span class="sxs-lookup"><span data-stu-id="d3a47-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="d3a47-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3a47-112">PARAMETERS</span></span>

### <span data-ttu-id="d3a47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a47-113">-DefaultProfile</span></span>
<span data-ttu-id="d3a47-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3a47-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3a47-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d3a47-115">-Name</span></span>
<span data-ttu-id="d3a47-116">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="d3a47-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="d3a47-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="d3a47-117">-Parameter</span></span>
<span data-ttu-id="d3a47-118">Parametername der Fabriceinstellung</span><span class="sxs-lookup"><span data-stu-id="d3a47-118">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="d3a47-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3a47-119">-ResourceGroupName</span></span>
<span data-ttu-id="d3a47-120">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d3a47-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d3a47-121">-Section</span><span class="sxs-lookup"><span data-stu-id="d3a47-121">-Section</span></span>
<span data-ttu-id="d3a47-122">Section name of the fabric setting</span><span class="sxs-lookup"><span data-stu-id="d3a47-122">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="d3a47-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="d3a47-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="d3a47-124">An array of fabric settings</span><span class="sxs-lookup"><span data-stu-id="d3a47-124">An array of fabric settings</span></span>

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

### <span data-ttu-id="d3a47-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3a47-125">-Confirm</span></span>
<span data-ttu-id="d3a47-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d3a47-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3a47-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d3a47-127">-WhatIf</span></span>
<span data-ttu-id="d3a47-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3a47-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3a47-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3a47-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3a47-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a47-130">CommonParameters</span></span>
<span data-ttu-id="d3a47-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3a47-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a47-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3a47-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a47-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d3a47-133">INPUTS</span></span>

### <span data-ttu-id="d3a47-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d3a47-134">System.String</span></span>

### <span data-ttu-id="d3a47-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span><span class="sxs-lookup"><span data-stu-id="d3a47-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="d3a47-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d3a47-136">OUTPUTS</span></span>

### <span data-ttu-id="d3a47-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="d3a47-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="d3a47-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d3a47-138">NOTES</span></span>

## <span data-ttu-id="d3a47-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d3a47-139">RELATED LINKS</span></span>
