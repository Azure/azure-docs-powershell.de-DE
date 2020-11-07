---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: 983edfae4876e2998d4134a679e76b64751ef0d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824707"
---
# <span data-ttu-id="eb827-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="eb827-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="eb827-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eb827-102">SYNOPSIS</span></span>
<span data-ttu-id="eb827-103">Erstellen eines neuen Service Fabric-Anwendungstyps unter der angegebenen Ressourcengruppe und dem angegebenen Cluster</span><span class="sxs-lookup"><span data-stu-id="eb827-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="eb827-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb827-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb827-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb827-105">DESCRIPTION</span></span>
<span data-ttu-id="eb827-106">Das Cmdlet erstellt einen neuen Dienst Fabric-Anwendungstyp unter der angegebenen Ressourcengruppe und dem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="eb827-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="eb827-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb827-107">EXAMPLES</span></span>

### <span data-ttu-id="eb827-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eb827-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="eb827-109">In diesem Beispiel wird ein neuer Anwendungstyp "testAppType" unter der angegebenen Ressourcengruppe und dem Cluster erstellt.</span><span class="sxs-lookup"><span data-stu-id="eb827-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="eb827-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb827-110">PARAMETERS</span></span>

### <span data-ttu-id="eb827-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="eb827-111">-ClusterName</span></span>
<span data-ttu-id="eb827-112">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="eb827-112">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="eb827-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb827-113">-DefaultProfile</span></span>
<span data-ttu-id="eb827-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eb827-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb827-115">-Name</span><span class="sxs-lookup"><span data-stu-id="eb827-115">-Name</span></span>
<span data-ttu-id="eb827-116">Geben Sie den Namen des Anwendungstyps an.</span><span class="sxs-lookup"><span data-stu-id="eb827-116">Specify the name of the application type</span></span>

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

### <span data-ttu-id="eb827-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb827-117">-ResourceGroupName</span></span>
<span data-ttu-id="eb827-118">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="eb827-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="eb827-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eb827-119">-Confirm</span></span>
<span data-ttu-id="eb827-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eb827-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb827-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb827-121">-WhatIf</span></span>
<span data-ttu-id="eb827-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eb827-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb827-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb827-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb827-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb827-124">CommonParameters</span></span>
<span data-ttu-id="eb827-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb827-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb827-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb827-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb827-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eb827-127">INPUTS</span></span>

### <span data-ttu-id="eb827-128">System. String</span><span class="sxs-lookup"><span data-stu-id="eb827-128">System.String</span></span>

## <span data-ttu-id="eb827-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eb827-129">OUTPUTS</span></span>

### <span data-ttu-id="eb827-130">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="eb827-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="eb827-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="eb827-131">NOTES</span></span>

## <span data-ttu-id="eb827-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eb827-132">RELATED LINKS</span></span>
