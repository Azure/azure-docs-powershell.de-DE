---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/add-azanalysisservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
ms.openlocfilehash: 523ccfb44d29473e41560de88d34519f98272375
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950395"
---
# <span data-ttu-id="cbf77-101">Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="cbf77-101">Add-AzAnalysisServicesAccount</span></span>

## <span data-ttu-id="cbf77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbf77-102">SYNOPSIS</span></span>
<span data-ttu-id="cbf77-103">Fügt ein authentifiziertes Konto hinzu, das für Azure Analysis Services-Server-Cmdletanforderungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cbf77-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

## <span data-ttu-id="cbf77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cbf77-104">SYNTAX</span></span>

### <span data-ttu-id="cbf77-105">UserParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="cbf77-105">UserParameterSetName (Default)</span></span>
```
Add-AzAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbf77-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="cbf77-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbf77-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="cbf77-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbf77-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cbf77-108">DESCRIPTION</span></span>
<span data-ttu-id="cbf77-109">Das Add-AzAnalysisServicesAccount-Cmdlet wird verwendet, um sich bei einer Instanz des Azure Analysis Services-Servers anzumelden.</span><span class="sxs-lookup"><span data-stu-id="cbf77-109">The Add-AzAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="cbf77-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cbf77-110">EXAMPLES</span></span>

### <span data-ttu-id="cbf77-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cbf77-111">Example 1</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="cbf77-112">In diesem Beispiel wird das von der $UserCredential-Variable angegebene Konto der westcentralus.asazure.windows.net Analysis Services-Umgebung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cbf77-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="cbf77-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cbf77-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="cbf77-114">Der erste Befehl ruft die Anmeldeinformationen des Anwendungsdienstprinzipals ab und speichert sie dann in der $ApplicationCredential Variablen.</span><span class="sxs-lookup"><span data-stu-id="cbf77-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="cbf77-115">Mit dem zweiten Befehl fügen Sie das anwendungsdienstprinzipalkonto hinzu, das von der $ApplicationCredential und TenantId der westcentralus.asazure.windows.net Analysis Services-Umgebung angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cbf77-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="cbf77-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="cbf77-116">Example 3</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="cbf77-117">In diesem Beispiel wird das Application Service Principal-Konto hinzugefügt, das von ApplicationId, TenantId und CertificateThumbprint angegeben ist, westcentralus.asazure.windows.net Analysis Services-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="cbf77-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="cbf77-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cbf77-118">PARAMETERS</span></span>

### <span data-ttu-id="cbf77-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="cbf77-119">-ApplicationId</span></span>
<span data-ttu-id="cbf77-120">Die Anwendungs-ID.</span><span class="sxs-lookup"><span data-stu-id="cbf77-120">The application ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf77-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="cbf77-121">-CertificateThumbprint</span></span>
<span data-ttu-id="cbf77-122">Zertifikathash (Fingerabdruck)</span><span class="sxs-lookup"><span data-stu-id="cbf77-122">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf77-123">-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="cbf77-123">-Credential</span></span>
<span data-ttu-id="cbf77-124">Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="cbf77-124">Login credentials</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithPasswordParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf77-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="cbf77-125">-RolloutEnvironment</span></span>
<span data-ttu-id="cbf77-126">Name der Azure Analysis Services-Umgebung, bei der sie sich anmeldet.</span><span class="sxs-lookup"><span data-stu-id="cbf77-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="cbf77-127">Wenn sie beispielsweise den vollständigen Namen des Servers asazure://westcentralus.asazure.windows.net/testserver, wird der richtige Wert für diese Variable westcentralus.asazure.windows.net</span><span class="sxs-lookup"><span data-stu-id="cbf77-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

```yaml
Type: System.String
Parameter Sets: UserParameterSetName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf77-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="cbf77-128">-ServicePrincipal</span></span>
<span data-ttu-id="cbf77-129">Gibt an, dass sich dieses Konto durch Bereitstellen von Dienstprinzipalanmeldeinformationen authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="cbf77-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf77-130">-TenantId</span><span class="sxs-lookup"><span data-stu-id="cbf77-130">-TenantId</span></span>
<span data-ttu-id="cbf77-131">Name oder ID des Mandanten</span><span class="sxs-lookup"><span data-stu-id="cbf77-131">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf77-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cbf77-132">-Confirm</span></span>
<span data-ttu-id="cbf77-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cbf77-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbf77-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbf77-134">-WhatIf</span></span>
<span data-ttu-id="cbf77-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cbf77-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbf77-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cbf77-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbf77-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbf77-137">CommonParameters</span></span>
<span data-ttu-id="cbf77-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbf77-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbf77-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbf77-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbf77-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cbf77-140">INPUTS</span></span>

### <span data-ttu-id="cbf77-141">Keine</span><span class="sxs-lookup"><span data-stu-id="cbf77-141">None</span></span>

## <span data-ttu-id="cbf77-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cbf77-142">OUTPUTS</span></span>

### <span data-ttu-id="cbf77-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="cbf77-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="cbf77-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="cbf77-144">NOTES</span></span>
<span data-ttu-id="cbf77-145">Alias: Login-AzAsAccount</span><span class="sxs-lookup"><span data-stu-id="cbf77-145">Alias: Login-AzAsAccount</span></span>

## <span data-ttu-id="cbf77-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="cbf77-146">RELATED LINKS</span></span>
