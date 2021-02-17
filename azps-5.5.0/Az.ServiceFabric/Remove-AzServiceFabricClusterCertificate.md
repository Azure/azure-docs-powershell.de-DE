---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 688ee9f8679a427d53319147e7d13fc9e1305277
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165060"
---
# <span data-ttu-id="d0554-101">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="d0554-101">Remove-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="d0554-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0554-102">SYNOPSIS</span></span>
<span data-ttu-id="d0554-103">Entfernen Sie ein Clusterzertifikat aus der Verwendung für cluster-Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="d0554-103">Remove a cluster certificate from being used for cluster security.</span></span>

## <span data-ttu-id="d0554-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0554-104">SYNTAX</span></span>

```
Remove-AzServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0554-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0554-105">DESCRIPTION</span></span>
<span data-ttu-id="d0554-106">Verwenden **Sie Remove-AzServiceFabricClusterCertificate,** um ein Clusterzertifikat aus dem Cluster zu entfernen, solange ein weiteres gültiges Zertifikat vorhanden ist, das bereits im Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d0554-106">Use **Remove-AzServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="d0554-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d0554-107">EXAMPLES</span></span>

### <span data-ttu-id="d0554-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d0554-108">Example 1</span></span>
```
PS C:\> Remove-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="d0554-109">Mit diesem Befehl wird das Zertifikat mit dem Fingerabdruck 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A aus der Clustersicherheit entfernt.</span><span class="sxs-lookup"><span data-stu-id="d0554-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="d0554-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0554-110">PARAMETERS</span></span>

### <span data-ttu-id="d0554-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0554-111">-DefaultProfile</span></span>
<span data-ttu-id="d0554-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0554-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0554-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d0554-113">-Name</span></span>
<span data-ttu-id="d0554-114">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="d0554-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d0554-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0554-115">-ResourceGroupName</span></span>
<span data-ttu-id="d0554-116">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d0554-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d0554-117">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="d0554-117">-Thumbprint</span></span>
<span data-ttu-id="d0554-118">Geben Sie den Clusterdrückdruck an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0554-118">Specify the cluster thumbprint which to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0554-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0554-119">-Confirm</span></span>
<span data-ttu-id="d0554-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d0554-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0554-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d0554-121">-WhatIf</span></span>
<span data-ttu-id="d0554-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d0554-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0554-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d0554-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0554-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0554-124">CommonParameters</span></span>
<span data-ttu-id="d0554-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0554-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0554-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0554-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0554-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d0554-127">INPUTS</span></span>

### <span data-ttu-id="d0554-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d0554-128">System.String</span></span>

## <span data-ttu-id="d0554-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d0554-129">OUTPUTS</span></span>

### <span data-ttu-id="d0554-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="d0554-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="d0554-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d0554-131">NOTES</span></span>

## <span data-ttu-id="d0554-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d0554-132">RELATED LINKS</span></span>
