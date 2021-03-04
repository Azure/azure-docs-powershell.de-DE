---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: f8724fe13cb44ac3e2640f747026c121303be252
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932232"
---
# <span data-ttu-id="9f817-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="9f817-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="9f817-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f817-102">SYNOPSIS</span></span>
<span data-ttu-id="9f817-103">Erstellen Sie einen neuen Service Fabric-Anwendungstyp unter der angegebenen Ressourcengruppe und dem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="9f817-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="9f817-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f817-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f817-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f817-105">DESCRIPTION</span></span>
<span data-ttu-id="9f817-106">Das Cmdlet erstellt einen neuen Service Fabric-Anwendungstyp unter der angegebenen Ressourcengruppe und dem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="9f817-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="9f817-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9f817-107">EXAMPLES</span></span>

### <span data-ttu-id="9f817-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9f817-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="9f817-109">In diesem Beispiel wird unter der angegebenen Ressourcengruppe und dem angegebenen Cluster der neue Anwendungstyp "testAppType" erstellt.</span><span class="sxs-lookup"><span data-stu-id="9f817-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="9f817-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9f817-110">PARAMETERS</span></span>

### <span data-ttu-id="9f817-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9f817-111">-ClusterName</span></span>
<span data-ttu-id="9f817-112">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="9f817-112">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f817-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f817-113">-DefaultProfile</span></span>
<span data-ttu-id="9f817-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f817-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f817-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9f817-115">-Name</span></span>
<span data-ttu-id="9f817-116">Angeben des Namens des Anwendungstyps</span><span class="sxs-lookup"><span data-stu-id="9f817-116">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f817-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f817-117">-ResourceGroupName</span></span>
<span data-ttu-id="9f817-118">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9f817-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="9f817-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9f817-119">-Confirm</span></span>
<span data-ttu-id="9f817-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f817-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f817-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f817-121">-WhatIf</span></span>
<span data-ttu-id="9f817-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f817-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f817-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f817-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f817-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f817-124">CommonParameters</span></span>
<span data-ttu-id="9f817-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f817-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f817-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f817-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f817-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9f817-127">INPUTS</span></span>

### <span data-ttu-id="9f817-128">System.String</span><span class="sxs-lookup"><span data-stu-id="9f817-128">System.String</span></span>

## <span data-ttu-id="9f817-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9f817-129">OUTPUTS</span></span>

### <span data-ttu-id="9f817-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="9f817-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="9f817-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9f817-131">NOTES</span></span>

## <span data-ttu-id="9f817-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9f817-132">RELATED LINKS</span></span>
