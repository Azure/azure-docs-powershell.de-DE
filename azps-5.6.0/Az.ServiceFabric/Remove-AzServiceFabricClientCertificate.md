---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: 1ed5b95346ffde947366696f30e54cfddcdea4d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945659"
---
# <span data-ttu-id="0b52c-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0b52c-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="0b52c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b52c-102">SYNOPSIS</span></span>
<span data-ttu-id="0b52c-103">Entfernen Sie die Namen von Clientzertifikaten oder Zertifikatsubjekten aus der Verwendung für die Clientauthentifizierung im Cluster.</span><span class="sxs-lookup"><span data-stu-id="0b52c-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="0b52c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b52c-104">SYNTAX</span></span>

### <span data-ttu-id="0b52c-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="0b52c-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b52c-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="0b52c-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b52c-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="0b52c-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b52c-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="0b52c-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b52c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b52c-109">DESCRIPTION</span></span>
<span data-ttu-id="0b52c-110">Verwenden **Sie Remove-AzServiceFabricClientCertificate,** um namen(n) eines Clientzertifikats oder eines Zertifikatsubjekts für die Clientauthentifizierung im Cluster zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="0b52c-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="0b52c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0b52c-111">EXAMPLES</span></span>

### <span data-ttu-id="0b52c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0b52c-112">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="0b52c-113">Mit diesem Befehl wird das Clientzertifikat mit dem Fingerabdruck '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' aus dem Cluster entfernt.</span><span class="sxs-lookup"><span data-stu-id="0b52c-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="0b52c-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0b52c-114">PARAMETERS</span></span>

### <span data-ttu-id="0b52c-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="0b52c-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="0b52c-116">Angeben des Clientzertifikat-Fingerabdrucks, der nur über Administratorberechtigungen verfügt</span><span class="sxs-lookup"><span data-stu-id="0b52c-116">Specify client certificate thumbprint which only has admin permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b52c-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="0b52c-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="0b52c-118">Angeben des allgemeinen Clientnamens, des Ausstellerfingerdrucks und des Authentifizierungstyps</span><span class="sxs-lookup"><span data-stu-id="0b52c-118">Specify client common name , issuer thumbprint and authentication type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b52c-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="0b52c-119">-CommonName</span></span>
<span data-ttu-id="0b52c-120">Geben Sie den allgemeinen Namen des Clientzertifikats an.</span><span class="sxs-lookup"><span data-stu-id="0b52c-120">Specify client certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b52c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b52c-121">-DefaultProfile</span></span>
<span data-ttu-id="0b52c-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b52c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b52c-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="0b52c-123">-IssuerThumbprint</span></span>
<span data-ttu-id="0b52c-124">Angeben des Fingerabdrucks des Ausstellers des Clientzertifikats</span><span class="sxs-lookup"><span data-stu-id="0b52c-124">Specify thumbprint of client certificate's issuer</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b52c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0b52c-125">-Name</span></span>
<span data-ttu-id="0b52c-126">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="0b52c-126">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="0b52c-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="0b52c-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="0b52c-128">Angeben des Clientzertifikat-Fingerabdrucks, der nur über schreibgeschützte Berechtigungen verfügt</span><span class="sxs-lookup"><span data-stu-id="0b52c-128">Specify client certificate thumbprint which only has read only permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b52c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b52c-129">-ResourceGroupName</span></span>
<span data-ttu-id="0b52c-130">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0b52c-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0b52c-131">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="0b52c-131">-Thumbprint</span></span>
<span data-ttu-id="0b52c-132">Angeben des Fingerabdrucks des Clientzertifikats</span><span class="sxs-lookup"><span data-stu-id="0b52c-132">Specify client certificate thumbprint</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b52c-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b52c-133">-Confirm</span></span>
<span data-ttu-id="0b52c-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b52c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b52c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b52c-135">-WhatIf</span></span>
<span data-ttu-id="0b52c-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b52c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b52c-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b52c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b52c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b52c-138">CommonParameters</span></span>
<span data-ttu-id="0b52c-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b52c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b52c-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b52c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b52c-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0b52c-141">INPUTS</span></span>

### <span data-ttu-id="0b52c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0b52c-142">System.String</span></span>

### <span data-ttu-id="0b52c-143">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0b52c-143">System.String[]</span></span>

### <span data-ttu-id="0b52c-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span><span class="sxs-lookup"><span data-stu-id="0b52c-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="0b52c-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0b52c-145">OUTPUTS</span></span>

### <span data-ttu-id="0b52c-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="0b52c-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="0b52c-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0b52c-147">NOTES</span></span>

## <span data-ttu-id="0b52c-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0b52c-148">RELATED LINKS</span></span>

[<span data-ttu-id="0b52c-149">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0b52c-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)
