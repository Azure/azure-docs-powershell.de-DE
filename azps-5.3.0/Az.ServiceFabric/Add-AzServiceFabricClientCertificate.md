---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: ca9dbbba29e6f770b727e1f96717c2626f112839
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471839"
---
# <span data-ttu-id="4ae16-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4ae16-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="4ae16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ae16-102">SYNOPSIS</span></span>
<span data-ttu-id="4ae16-103">Fügen Sie dem Cluster zu Clientauthentifizierungszwecken allgemeinen Namen oder Fingerabdrück hinzu.</span><span class="sxs-lookup"><span data-stu-id="4ae16-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="4ae16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ae16-104">SYNTAX</span></span>

### <span data-ttu-id="4ae16-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="4ae16-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ae16-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="4ae16-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ae16-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="4ae16-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ae16-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="4ae16-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ae16-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ae16-109">DESCRIPTION</span></span>
<span data-ttu-id="4ae16-110">Verwenden **Sie "Add-AzServiceFabricClientCertificate",** um dem Cluster einen allgemeinen Namen und einen Aussteller des Fingerabdrucks oder Zertifikatabdrucks hinzuzufügen, damit der Client ihn für die Authentifizierung verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="4ae16-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="4ae16-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4ae16-111">EXAMPLES</span></span>

### <span data-ttu-id="4ae16-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ae16-112">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="4ae16-113">Mit diesem Befehl wird dem Cluster das Zertifikat mit dem Fingerabdruck '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' hinzugefügt, damit der Client das Zertifikat als Administrator für die Kommunikation mit dem Cluster verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="4ae16-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="4ae16-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4ae16-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="4ae16-115">Mit diesem Befehl wird ein schreibgeschütztes Clientzertifikat mit dem allgemeinen Namen "Contoso.com" und dem Aussteller "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" für den Cluster hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4ae16-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="4ae16-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ae16-116">PARAMETERS</span></span>

### <span data-ttu-id="4ae16-117">-Admin</span><span class="sxs-lookup"><span data-stu-id="4ae16-117">-Admin</span></span>
<span data-ttu-id="4ae16-118">Clientauthentifizierungstyp</span><span class="sxs-lookup"><span data-stu-id="4ae16-118">Client authentication type</span></span>

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

### <span data-ttu-id="4ae16-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="4ae16-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="4ae16-120">Angeben des Fingerabdruckdrucks für das Clientzertifikat, das nur über Administratorberechtigungen verfügt</span><span class="sxs-lookup"><span data-stu-id="4ae16-120">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="4ae16-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="4ae16-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="4ae16-122">Angeben des allgemeinen Clientnamens, des Ausstellers von Thumbprint und des Authentifizierungstyps</span><span class="sxs-lookup"><span data-stu-id="4ae16-122">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="4ae16-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="4ae16-123">-CommonName</span></span>
<span data-ttu-id="4ae16-124">Geben Sie den allgemeinen Namen des Clientzertifikats an.</span><span class="sxs-lookup"><span data-stu-id="4ae16-124">Specify client certificate common name</span></span>

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

### <span data-ttu-id="4ae16-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ae16-125">-DefaultProfile</span></span>
<span data-ttu-id="4ae16-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ae16-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ae16-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="4ae16-127">-IssuerThumbprint</span></span>
<span data-ttu-id="4ae16-128">Angeben des Fingerabdruckdrucks des Ausstellers des Clientzertifikats</span><span class="sxs-lookup"><span data-stu-id="4ae16-128">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="4ae16-129">-Name</span><span class="sxs-lookup"><span data-stu-id="4ae16-129">-Name</span></span>
<span data-ttu-id="4ae16-130">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="4ae16-130">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="4ae16-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="4ae16-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="4ae16-132">Angeben des Fingerabdruckdrucks für das Clientzertifikat, der nur über die Berechtigung "Nur lesen" verfügt</span><span class="sxs-lookup"><span data-stu-id="4ae16-132">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="4ae16-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ae16-133">-ResourceGroupName</span></span>
<span data-ttu-id="4ae16-134">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4ae16-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="4ae16-135">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="4ae16-135">-Thumbprint</span></span>
<span data-ttu-id="4ae16-136">Angeben des Fingerabdruckdrucks für das Clientzertifikat</span><span class="sxs-lookup"><span data-stu-id="4ae16-136">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="4ae16-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ae16-137">-Confirm</span></span>
<span data-ttu-id="4ae16-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ae16-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ae16-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4ae16-139">-WhatIf</span></span>
<span data-ttu-id="4ae16-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ae16-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ae16-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ae16-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ae16-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ae16-142">CommonParameters</span></span>
<span data-ttu-id="4ae16-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ae16-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ae16-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ae16-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ae16-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4ae16-145">INPUTS</span></span>

### <span data-ttu-id="4ae16-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4ae16-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4ae16-147">System.String</span><span class="sxs-lookup"><span data-stu-id="4ae16-147">System.String</span></span>

### <span data-ttu-id="4ae16-148">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4ae16-148">System.String[]</span></span>

### <span data-ttu-id="4ae16-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span><span class="sxs-lookup"><span data-stu-id="4ae16-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="4ae16-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4ae16-150">OUTPUTS</span></span>

### <span data-ttu-id="4ae16-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="4ae16-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="4ae16-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4ae16-152">NOTES</span></span>

## <span data-ttu-id="4ae16-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4ae16-153">RELATED LINKS</span></span>

[<span data-ttu-id="4ae16-154">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4ae16-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)
