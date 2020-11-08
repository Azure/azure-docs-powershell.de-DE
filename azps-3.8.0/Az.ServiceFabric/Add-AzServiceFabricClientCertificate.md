---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: 913b610bc1d79c7a1792c06b53947fd3bf51151a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995575"
---
# <span data-ttu-id="6907e-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6907e-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="6907e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6907e-102">SYNOPSIS</span></span>
<span data-ttu-id="6907e-103">Fügen Sie dem Cluster einen allgemeinen Namen oder Fingerabdruck hinzu, um Client Authentifizierungszwecke zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6907e-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="6907e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6907e-104">SYNTAX</span></span>

### <span data-ttu-id="6907e-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="6907e-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6907e-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="6907e-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6907e-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="6907e-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6907e-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="6907e-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6907e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6907e-109">DESCRIPTION</span></span>
<span data-ttu-id="6907e-110">Verwenden Sie **Add-AzServiceFabricClientCertificate** , um dem Cluster einen allgemeinen Namen und einen ausstellenden Fingerabdruck oder Zertifikat Fingerabdruck hinzuzufügen, damit der Client ihn zur Authentifizierung verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="6907e-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="6907e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6907e-111">EXAMPLES</span></span>

### <span data-ttu-id="6907e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6907e-112">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="6907e-113">Mit diesem Befehl wird dem Cluster das Zertifikat mit dem Fingerabdruck "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" hinzugefügt, sodass der Client das Zertifikat als Administrator für die Kommunikation mit dem Cluster verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="6907e-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="6907e-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6907e-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="6907e-115">Mit diesem Befehl wird ein nur-Lese-Clientzertifikat hinzugefügt, dessen allgemeiner Name "contoso.com" und der Fingerabdruck des Ausstellers "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" ist.</span><span class="sxs-lookup"><span data-stu-id="6907e-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="6907e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="6907e-116">PARAMETERS</span></span>

### <span data-ttu-id="6907e-117">– Administrator</span><span class="sxs-lookup"><span data-stu-id="6907e-117">-Admin</span></span>
<span data-ttu-id="6907e-118">Client Authentifizierungstyp</span><span class="sxs-lookup"><span data-stu-id="6907e-118">Client authentication type</span></span>

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

### <span data-ttu-id="6907e-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="6907e-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="6907e-120">Clientzertifikat-Fingerabdruck angeben, der nur über Administratorberechtigungen verfügt</span><span class="sxs-lookup"><span data-stu-id="6907e-120">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="6907e-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="6907e-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="6907e-122">Angeben des gemeinsamen Client namens, des Ausstellers und des Authentifizierungstyps</span><span class="sxs-lookup"><span data-stu-id="6907e-122">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="6907e-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="6907e-123">-CommonName</span></span>
<span data-ttu-id="6907e-124">Allgemeinen Namen des Clientzertifikats angeben</span><span class="sxs-lookup"><span data-stu-id="6907e-124">Specify client certificate common name</span></span>

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

### <span data-ttu-id="6907e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6907e-125">-DefaultProfile</span></span>
<span data-ttu-id="6907e-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6907e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6907e-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="6907e-127">-IssuerThumbprint</span></span>
<span data-ttu-id="6907e-128">Angeben des Fingerabdrucks für den Aussteller des Clientzertifikats</span><span class="sxs-lookup"><span data-stu-id="6907e-128">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="6907e-129">-Name</span><span class="sxs-lookup"><span data-stu-id="6907e-129">-Name</span></span>
<span data-ttu-id="6907e-130">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="6907e-130">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="6907e-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="6907e-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="6907e-132">Clientzertifikat-Fingerabdruck angeben, der nur die Berechtigung "nur lesen" hat</span><span class="sxs-lookup"><span data-stu-id="6907e-132">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="6907e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6907e-133">-ResourceGroupName</span></span>
<span data-ttu-id="6907e-134">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="6907e-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="6907e-135">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="6907e-135">-Thumbprint</span></span>
<span data-ttu-id="6907e-136">Angeben des Fingerabdrucks für ein Clientzertifikat</span><span class="sxs-lookup"><span data-stu-id="6907e-136">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="6907e-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6907e-137">-Confirm</span></span>
<span data-ttu-id="6907e-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6907e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6907e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6907e-139">-WhatIf</span></span>
<span data-ttu-id="6907e-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6907e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6907e-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6907e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6907e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6907e-142">CommonParameters</span></span>
<span data-ttu-id="6907e-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6907e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6907e-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6907e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6907e-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6907e-145">INPUTS</span></span>

### <span data-ttu-id="6907e-146">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="6907e-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6907e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="6907e-147">System.String</span></span>

### <span data-ttu-id="6907e-148">System. String []</span><span class="sxs-lookup"><span data-stu-id="6907e-148">System.String[]</span></span>

### <span data-ttu-id="6907e-149">Microsoft. Azure. Commands. ServiceFabric. Models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="6907e-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="6907e-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6907e-150">OUTPUTS</span></span>

### <span data-ttu-id="6907e-151">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="6907e-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="6907e-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="6907e-152">NOTES</span></span>

## <span data-ttu-id="6907e-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6907e-153">RELATED LINKS</span></span>

[<span data-ttu-id="6907e-154">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6907e-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)
