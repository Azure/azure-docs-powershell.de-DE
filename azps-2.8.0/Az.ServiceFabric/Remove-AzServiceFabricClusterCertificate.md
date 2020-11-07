---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: e29ee3c51b94964db286a999630196b46ad9f786
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823167"
---
# <span data-ttu-id="7c703-101">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="7c703-101">Remove-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="7c703-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7c703-102">SYNOPSIS</span></span>
<span data-ttu-id="7c703-103">Entfernen Sie ein Cluster Zertifikat, das für die Cluster Sicherheit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7c703-103">Remove a cluster certificate from being used for cluster security.</span></span>

## <span data-ttu-id="7c703-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c703-104">SYNTAX</span></span>

```
Remove-AzServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c703-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c703-105">DESCRIPTION</span></span>
<span data-ttu-id="7c703-106">Verwenden **Sie Remove-AzServiceFabricClusterCertificate** , um ein Cluster Zertifikat aus dem Cluster zu entfernen, sofern noch ein weiteres gültiges Zertifikat vorhanden ist, das bereits im Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7c703-106">Use **Remove-AzServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="7c703-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c703-107">EXAMPLES</span></span>

### <span data-ttu-id="7c703-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7c703-108">Example 1</span></span>
```
PS C:\> Remove-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="7c703-109">Mit diesem Befehl wird das Zertifikat mit dem Fingerabdruck-5F3660C715EBBDA31DB1FFDCF508302348DE8E7A für die Cluster Sicherheit entfernt.</span><span class="sxs-lookup"><span data-stu-id="7c703-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="7c703-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c703-110">PARAMETERS</span></span>

### <span data-ttu-id="7c703-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c703-111">-DefaultProfile</span></span>
<span data-ttu-id="7c703-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7c703-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c703-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7c703-113">-Name</span></span>
<span data-ttu-id="7c703-114">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="7c703-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="7c703-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c703-115">-ResourceGroupName</span></span>
<span data-ttu-id="7c703-116">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7c703-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7c703-117">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="7c703-117">-Thumbprint</span></span>
<span data-ttu-id="7c703-118">Geben Sie den zu entfernenden Cluster-Fingerabdruck an.</span><span class="sxs-lookup"><span data-stu-id="7c703-118">Specify the cluster thumbprint which to be removed.</span></span>

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

### <span data-ttu-id="7c703-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7c703-119">-Confirm</span></span>
<span data-ttu-id="7c703-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c703-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c703-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c703-121">-WhatIf</span></span>
<span data-ttu-id="7c703-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c703-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c703-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c703-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c703-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c703-124">CommonParameters</span></span>
<span data-ttu-id="7c703-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c703-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c703-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c703-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c703-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7c703-127">INPUTS</span></span>

### <span data-ttu-id="7c703-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7c703-128">System.String</span></span>

## <span data-ttu-id="7c703-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7c703-129">OUTPUTS</span></span>

### <span data-ttu-id="7c703-130">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="7c703-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="7c703-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c703-131">NOTES</span></span>

## <span data-ttu-id="7c703-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7c703-132">RELATED LINKS</span></span>
