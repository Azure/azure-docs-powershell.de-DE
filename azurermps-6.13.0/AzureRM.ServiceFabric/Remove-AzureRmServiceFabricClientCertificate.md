---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: 369c642485e3c83f4eaf6dee986beca676ea5051
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664322"
---
# <span data-ttu-id="e62e8-101">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e62e8-101">Remove-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="e62e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e62e8-102">SYNOPSIS</span></span>
<span data-ttu-id="e62e8-103">Entfernen Sie ein Clientzertifikat (e) oder den Namen des Zertifikats betreffs, der für die Clientauthentifizierung für den Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e62e8-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e62e8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e62e8-104">SYNTAX</span></span>

### <span data-ttu-id="e62e8-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="e62e8-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e62e8-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="e62e8-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e62e8-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="e62e8-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e62e8-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="e62e8-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e62e8-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e62e8-109">DESCRIPTION</span></span>
<span data-ttu-id="e62e8-110">Verwenden **Sie Remove-AzureRmServiceFabricClientCertificate** , um ein Clientzertifikat (e) oder den Namen der Zertifikats Subjekte (n) zu entfernen, die für die Clientauthentifizierung für den Cluster verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e62e8-110">Use **Remove-AzureRmServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="e62e8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e62e8-111">EXAMPLES</span></span>

### <span data-ttu-id="e62e8-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e62e8-112">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="e62e8-113">Mit diesem Befehl wird das Clientzertifikat mit dem Fingerabdruck "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" aus dem Cluster entfernt.</span><span class="sxs-lookup"><span data-stu-id="e62e8-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="e62e8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e62e8-114">PARAMETERS</span></span>

### <span data-ttu-id="e62e8-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="e62e8-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="e62e8-116">Geben Sie den Fingerabdruck des Clientzertifikats an, der nur über Administratorberechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="e62e8-116">Specify client certificate thumbprint that only has admin permission.</span></span>

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

### <span data-ttu-id="e62e8-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="e62e8-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="e62e8-118">Geben Sie den allgemeinen Clientnamen, den Aussteller Fingerabdruck und den Authentifizierungstyp an.</span><span class="sxs-lookup"><span data-stu-id="e62e8-118">Specify client common name, issuer thumbprint, and authentication type.</span></span>

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

### <span data-ttu-id="e62e8-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="e62e8-119">-CommonName</span></span>
<span data-ttu-id="e62e8-120">Geben Sie den allgemeinen Namen des Clientzertifikats an.</span><span class="sxs-lookup"><span data-stu-id="e62e8-120">Specify client certificate common name.</span></span>

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

### <span data-ttu-id="e62e8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e62e8-121">-DefaultProfile</span></span>
<span data-ttu-id="e62e8-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e62e8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62e8-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="e62e8-123">-IssuerThumbprint</span></span>
<span data-ttu-id="e62e8-124">Geben Sie den Fingerabdruck des Clientzertifikats heraus.</span><span class="sxs-lookup"><span data-stu-id="e62e8-124">Specify client certificate issuer thumbprint.</span></span>

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

### <span data-ttu-id="e62e8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e62e8-125">-Name</span></span>
<span data-ttu-id="e62e8-126">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="e62e8-126">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e62e8-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="e62e8-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="e62e8-128">Geben Sie den Fingerabdruck des Clientzertifikats an, der nur die Berechtigung Lesen hat.</span><span class="sxs-lookup"><span data-stu-id="e62e8-128">Specify client certificate thumbprint that has read only permission.</span></span>

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

### <span data-ttu-id="e62e8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e62e8-129">-ResourceGroupName</span></span>
<span data-ttu-id="e62e8-130">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e62e8-130">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e62e8-131">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="e62e8-131">-Thumbprint</span></span>
<span data-ttu-id="e62e8-132">Kunden Zertifikat-Fingerabdruck angeben.</span><span class="sxs-lookup"><span data-stu-id="e62e8-132">Specify client certificate thumbprint.</span></span>

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

### <span data-ttu-id="e62e8-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e62e8-133">-Confirm</span></span>
<span data-ttu-id="e62e8-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e62e8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e62e8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e62e8-135">-WhatIf</span></span>
<span data-ttu-id="e62e8-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e62e8-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e62e8-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e62e8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e62e8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e62e8-138">CommonParameters</span></span>
<span data-ttu-id="e62e8-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e62e8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e62e8-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e62e8-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e62e8-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e62e8-141">INPUTS</span></span>

### <span data-ttu-id="e62e8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e62e8-142">System.String</span></span>
<span data-ttu-id="e62e8-143">Parameter: CommonName (ByValue), IssuerThumbprint (ByValue), Fingerabdruck (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e62e8-143">Parameters: CommonName (ByValue), IssuerThumbprint (ByValue), Thumbprint (ByValue)</span></span>

### <span data-ttu-id="e62e8-144">System. String []</span><span class="sxs-lookup"><span data-stu-id="e62e8-144">System.String[]</span></span>
<span data-ttu-id="e62e8-145">Parameter: AdminClientThumbprint (ByValue), ReadonlyClientThumbprint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e62e8-145">Parameters: AdminClientThumbprint (ByValue), ReadonlyClientThumbprint (ByValue)</span></span>

### <span data-ttu-id="e62e8-146">Microsoft. Azure. Commands. ServiceFabric. Models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="e62e8-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>
<span data-ttu-id="e62e8-147">Parameter: ClientCertificateCommonName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e62e8-147">Parameters: ClientCertificateCommonName (ByValue)</span></span>

## <span data-ttu-id="e62e8-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e62e8-148">OUTPUTS</span></span>

### <span data-ttu-id="e62e8-149">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="e62e8-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="e62e8-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="e62e8-150">NOTES</span></span>

## <span data-ttu-id="e62e8-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e62e8-151">RELATED LINKS</span></span>

[<span data-ttu-id="e62e8-152">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e62e8-152">Add-AzureRmServiceFabricClientCertificate</span></span>](./Add-AzureRmServiceFabricClientCertificate.md)
