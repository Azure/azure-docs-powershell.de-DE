---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 688ee9f8679a427d53319147e7d13fc9e1305277
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174162"
---
# <span data-ttu-id="fc57f-101">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="fc57f-101">Remove-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="fc57f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fc57f-102">SYNOPSIS</span></span>
<span data-ttu-id="fc57f-103">Entfernen Sie ein Cluster Zertifikat, das für die Cluster Sicherheit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fc57f-103">Remove a cluster certificate from being used for cluster security.</span></span>

## <span data-ttu-id="fc57f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc57f-104">SYNTAX</span></span>

```
Remove-AzServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc57f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc57f-105">DESCRIPTION</span></span>
<span data-ttu-id="fc57f-106">Verwenden **Sie Remove-AzServiceFabricClusterCertificate** , um ein Cluster Zertifikat aus dem Cluster zu entfernen, sofern noch ein weiteres gültiges Zertifikat vorhanden ist, das bereits im Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fc57f-106">Use **Remove-AzServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="fc57f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc57f-107">EXAMPLES</span></span>

### <span data-ttu-id="fc57f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fc57f-108">Example 1</span></span>
```
PS C:\> Remove-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="fc57f-109">Mit diesem Befehl wird das Zertifikat mit dem Fingerabdruck-5F3660C715EBBDA31DB1FFDCF508302348DE8E7A für die Cluster Sicherheit entfernt.</span><span class="sxs-lookup"><span data-stu-id="fc57f-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="fc57f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc57f-110">PARAMETERS</span></span>

### <span data-ttu-id="fc57f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc57f-111">-DefaultProfile</span></span>
<span data-ttu-id="fc57f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fc57f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc57f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="fc57f-113">-Name</span></span>
<span data-ttu-id="fc57f-114">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="fc57f-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="fc57f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc57f-115">-ResourceGroupName</span></span>
<span data-ttu-id="fc57f-116">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="fc57f-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fc57f-117">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="fc57f-117">-Thumbprint</span></span>
<span data-ttu-id="fc57f-118">Geben Sie den zu entfernenden Cluster-Fingerabdruck an.</span><span class="sxs-lookup"><span data-stu-id="fc57f-118">Specify the cluster thumbprint which to be removed.</span></span>

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

### <span data-ttu-id="fc57f-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fc57f-119">-Confirm</span></span>
<span data-ttu-id="fc57f-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc57f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc57f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc57f-121">-WhatIf</span></span>
<span data-ttu-id="fc57f-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc57f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc57f-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc57f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc57f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc57f-124">CommonParameters</span></span>
<span data-ttu-id="fc57f-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc57f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc57f-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc57f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc57f-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fc57f-127">INPUTS</span></span>

### <span data-ttu-id="fc57f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fc57f-128">System.String</span></span>

## <span data-ttu-id="fc57f-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fc57f-129">OUTPUTS</span></span>

### <span data-ttu-id="fc57f-130">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="fc57f-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="fc57f-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="fc57f-131">NOTES</span></span>

## <span data-ttu-id="fc57f-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fc57f-132">RELATED LINKS</span></span>
