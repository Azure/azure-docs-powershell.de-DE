---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 59f8723470707a644e426bd9559a8e982f731e6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945658"
---
# <span data-ttu-id="f6f2b-101">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f6f2b-101">Remove-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="f6f2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6f2b-102">SYNOPSIS</span></span>
<span data-ttu-id="f6f2b-103">Entfernen Sie ein Clusterzertifikat aus der Verwendung für die Clustersicherheit.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-103">Remove a cluster certificate from being used for cluster security.</span></span>

## <span data-ttu-id="f6f2b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6f2b-104">SYNTAX</span></span>

```
Remove-AzServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6f2b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6f2b-105">DESCRIPTION</span></span>
<span data-ttu-id="f6f2b-106">Verwenden **Sie Remove-AzServiceFabricClusterCertificate,** um ein Clusterzertifikat aus dem Cluster zu entfernen, solange ein weiteres gültiges Zertifikat vorhanden ist, das bereits im Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-106">Use **Remove-AzServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="f6f2b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f6f2b-107">EXAMPLES</span></span>

### <span data-ttu-id="f6f2b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f6f2b-108">Example 1</span></span>
```
PS C:\> Remove-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="f6f2b-109">Mit diesem Befehl wird das Zertifikat mit dem Fingerabdruck 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A für die Clustersicherheit entfernt.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="f6f2b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f6f2b-110">PARAMETERS</span></span>

### <span data-ttu-id="f6f2b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6f2b-111">-DefaultProfile</span></span>
<span data-ttu-id="f6f2b-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6f2b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f6f2b-113">-Name</span></span>
<span data-ttu-id="f6f2b-114">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="f6f2b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6f2b-115">-ResourceGroupName</span></span>
<span data-ttu-id="f6f2b-116">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f6f2b-117">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="f6f2b-117">-Thumbprint</span></span>
<span data-ttu-id="f6f2b-118">Geben Sie den cluster thumbprint an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-118">Specify the cluster thumbprint which to be removed.</span></span>

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

### <span data-ttu-id="f6f2b-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f6f2b-119">-Confirm</span></span>
<span data-ttu-id="f6f2b-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6f2b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6f2b-121">-WhatIf</span></span>
<span data-ttu-id="f6f2b-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6f2b-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6f2b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6f2b-124">CommonParameters</span></span>
<span data-ttu-id="f6f2b-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6f2b-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6f2b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6f2b-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f6f2b-127">INPUTS</span></span>

### <span data-ttu-id="f6f2b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f6f2b-128">System.String</span></span>

## <span data-ttu-id="f6f2b-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f6f2b-129">OUTPUTS</span></span>

### <span data-ttu-id="f6f2b-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="f6f2b-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="f6f2b-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f6f2b-131">NOTES</span></span>

## <span data-ttu-id="f6f2b-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f6f2b-132">RELATED LINKS</span></span>
