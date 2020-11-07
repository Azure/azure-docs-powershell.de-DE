---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: d2488792b5893e3972aa27ce98f87a23cec23073
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823168"
---
# <span data-ttu-id="b076b-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b076b-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="b076b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b076b-102">SYNOPSIS</span></span>
<span data-ttu-id="b076b-103">Entfernen Sie ein Clientzertifikat (e) oder den Namen des Zertifikats betreffs, der für die Clientauthentifizierung für den Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b076b-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="b076b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b076b-104">SYNTAX</span></span>

### <span data-ttu-id="b076b-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="b076b-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b076b-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="b076b-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b076b-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="b076b-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b076b-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="b076b-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b076b-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b076b-109">DESCRIPTION</span></span>
<span data-ttu-id="b076b-110">Verwenden **Sie Remove-AzServiceFabricClientCertificate** , um ein Clientzertifikat (e) oder den Namen der Zertifikats Subjekte (n) zu entfernen, die für die Clientauthentifizierung für den Cluster verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b076b-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="b076b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b076b-111">EXAMPLES</span></span>

### <span data-ttu-id="b076b-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b076b-112">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="b076b-113">Mit diesem Befehl wird das Clientzertifikat mit dem Fingerabdruck "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" aus dem Cluster entfernt.</span><span class="sxs-lookup"><span data-stu-id="b076b-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="b076b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b076b-114">PARAMETERS</span></span>

### <span data-ttu-id="b076b-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="b076b-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="b076b-116">Clientzertifikat-Fingerabdruck angeben, der nur über Administratorberechtigungen verfügt</span><span class="sxs-lookup"><span data-stu-id="b076b-116">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="b076b-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="b076b-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="b076b-118">Angeben des gemeinsamen Client namens, des Ausstellers und des Authentifizierungstyps</span><span class="sxs-lookup"><span data-stu-id="b076b-118">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="b076b-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="b076b-119">-CommonName</span></span>
<span data-ttu-id="b076b-120">Allgemeinen Namen des Clientzertifikats angeben</span><span class="sxs-lookup"><span data-stu-id="b076b-120">Specify client certificate common name</span></span>

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

### <span data-ttu-id="b076b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b076b-121">-DefaultProfile</span></span>
<span data-ttu-id="b076b-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b076b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b076b-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="b076b-123">-IssuerThumbprint</span></span>
<span data-ttu-id="b076b-124">Angeben des Fingerabdrucks für den Aussteller des Clientzertifikats</span><span class="sxs-lookup"><span data-stu-id="b076b-124">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="b076b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b076b-125">-Name</span></span>
<span data-ttu-id="b076b-126">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="b076b-126">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="b076b-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="b076b-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="b076b-128">Clientzertifikat-Fingerabdruck angeben, der nur die Berechtigung "nur lesen" hat</span><span class="sxs-lookup"><span data-stu-id="b076b-128">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="b076b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b076b-129">-ResourceGroupName</span></span>
<span data-ttu-id="b076b-130">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b076b-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b076b-131">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="b076b-131">-Thumbprint</span></span>
<span data-ttu-id="b076b-132">Angeben des Fingerabdrucks für ein Clientzertifikat</span><span class="sxs-lookup"><span data-stu-id="b076b-132">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="b076b-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b076b-133">-Confirm</span></span>
<span data-ttu-id="b076b-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b076b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b076b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b076b-135">-WhatIf</span></span>
<span data-ttu-id="b076b-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b076b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b076b-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b076b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b076b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b076b-138">CommonParameters</span></span>
<span data-ttu-id="b076b-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b076b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b076b-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b076b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b076b-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b076b-141">INPUTS</span></span>

### <span data-ttu-id="b076b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b076b-142">System.String</span></span>

### <span data-ttu-id="b076b-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="b076b-143">System.String[]</span></span>

### <span data-ttu-id="b076b-144">Microsoft. Azure. Commands. ServiceFabric. Models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="b076b-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="b076b-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b076b-145">OUTPUTS</span></span>

### <span data-ttu-id="b076b-146">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="b076b-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="b076b-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="b076b-147">NOTES</span></span>

## <span data-ttu-id="b076b-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b076b-148">RELATED LINKS</span></span>

[<span data-ttu-id="b076b-149">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b076b-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)
