---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: bb6280eb623f52256eda5324e3d7980894fc91e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659334"
---
# <span data-ttu-id="fd267-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="fd267-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="fd267-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd267-102">SYNOPSIS</span></span>
<span data-ttu-id="fd267-103">Fügen Sie dem Cluster einen allgemeinen Namen oder Fingerabdruck hinzu, um Client Authentifizierungszwecke zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fd267-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="fd267-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd267-104">SYNTAX</span></span>

### <span data-ttu-id="fd267-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="fd267-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd267-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="fd267-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd267-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="fd267-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd267-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="fd267-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd267-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd267-109">DESCRIPTION</span></span>
<span data-ttu-id="fd267-110">Verwenden Sie **Add-AzServiceFabricClientCertificate** , um dem Cluster einen allgemeinen Namen und einen ausstellenden Fingerabdruck oder Zertifikat Fingerabdruck hinzuzufügen, damit der Client ihn zur Authentifizierung verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="fd267-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="fd267-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd267-111">EXAMPLES</span></span>

### <span data-ttu-id="fd267-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fd267-112">Example 1</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="fd267-113">Mit diesem Befehl wird dem Cluster das Zertifikat mit dem Fingerabdruck "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" hinzugefügt, sodass der Client das Zertifikat als Administrator für die Kommunikation mit dem Cluster verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="fd267-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="fd267-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fd267-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="fd267-115">Mit diesem Befehl wird ein nur-Lese-Clientzertifikat hinzugefügt, dessen allgemeiner Name "contoso.com" und der Fingerabdruck des Ausstellers "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" ist.</span><span class="sxs-lookup"><span data-stu-id="fd267-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="fd267-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd267-116">PARAMETERS</span></span>

### <span data-ttu-id="fd267-117">– Administrator</span><span class="sxs-lookup"><span data-stu-id="fd267-117">-Admin</span></span>
<span data-ttu-id="fd267-118">Client Authentifizierungs.</span><span class="sxs-lookup"><span data-stu-id="fd267-118">Client authentication type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd267-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="fd267-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="fd267-120">Geben Sie den Fingerabdruck des Clientzertifikats an, der nur über Administratorberechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="fd267-120">Specify client certificate thumbprint that only has admin permission.</span></span>

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

### <span data-ttu-id="fd267-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="fd267-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="fd267-122">Geben Sie den allgemeinen Clientnamen, den Aussteller Fingerabdruck und den Authentifizierungstyp an.</span><span class="sxs-lookup"><span data-stu-id="fd267-122">Specify client common name, issuer thumbprint, and authentication type.</span></span>

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

### <span data-ttu-id="fd267-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="fd267-123">-CommonName</span></span>
<span data-ttu-id="fd267-124">Geben Sie den allgemeinen Namen des Clientzertifikats an.</span><span class="sxs-lookup"><span data-stu-id="fd267-124">Specify client certificate common name.</span></span>

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

### <span data-ttu-id="fd267-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd267-125">-DefaultProfile</span></span>
<span data-ttu-id="fd267-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fd267-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd267-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="fd267-127">-IssuerThumbprint</span></span>
<span data-ttu-id="fd267-128">Geben Sie den Fingerabdruck des Clientzertifikats heraus.</span><span class="sxs-lookup"><span data-stu-id="fd267-128">Specify client certificate issuer thumbprint.</span></span>

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

### <span data-ttu-id="fd267-129">-Name</span><span class="sxs-lookup"><span data-stu-id="fd267-129">-Name</span></span>
<span data-ttu-id="fd267-130">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="fd267-130">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="fd267-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="fd267-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="fd267-132">Geben Sie den Fingerabdruck des Clientzertifikats an, der nur die Berechtigung Lesen hat.</span><span class="sxs-lookup"><span data-stu-id="fd267-132">Specify client certificate thumbprint that has read only permission.</span></span>

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

### <span data-ttu-id="fd267-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd267-133">-ResourceGroupName</span></span>
<span data-ttu-id="fd267-134">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="fd267-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fd267-135">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="fd267-135">-Thumbprint</span></span>
<span data-ttu-id="fd267-136">Kunden Zertifikat-Fingerabdruck angeben.</span><span class="sxs-lookup"><span data-stu-id="fd267-136">Specify client certificate thumbprint.</span></span>

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

### <span data-ttu-id="fd267-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fd267-137">-Confirm</span></span>
<span data-ttu-id="fd267-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd267-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd267-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd267-139">-WhatIf</span></span>
<span data-ttu-id="fd267-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd267-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd267-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd267-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd267-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd267-142">CommonParameters</span></span>
<span data-ttu-id="fd267-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd267-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd267-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd267-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd267-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd267-145">INPUTS</span></span>

### <span data-ttu-id="fd267-146">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="fd267-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="fd267-147">System. String</span><span class="sxs-lookup"><span data-stu-id="fd267-147">System.String</span></span>

### <span data-ttu-id="fd267-148">System. String []</span><span class="sxs-lookup"><span data-stu-id="fd267-148">System.String[]</span></span>

### <span data-ttu-id="fd267-149">Microsoft. Azure. Commands. ServiceFabric. Models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="fd267-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="fd267-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd267-150">OUTPUTS</span></span>

### <span data-ttu-id="fd267-151">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="fd267-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="fd267-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd267-152">NOTES</span></span>

## <span data-ttu-id="fd267-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd267-153">RELATED LINKS</span></span>

[<span data-ttu-id="fd267-154">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="fd267-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)
