---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/add-azanalysisservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
ms.openlocfilehash: f1d59a0a34072a91242c6595c269ba55c4397e0e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290891"
---
# <span data-ttu-id="53792-101">Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="53792-101">Add-AzAnalysisServicesAccount</span></span>

## <span data-ttu-id="53792-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53792-102">SYNOPSIS</span></span>
<span data-ttu-id="53792-103">Fügt ein authentifiziertes Konto hinzu, das für Azure Analysis Services-Server-Cmdlet-Anforderungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="53792-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

## <span data-ttu-id="53792-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53792-104">SYNTAX</span></span>

### <span data-ttu-id="53792-105">UserParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="53792-105">UserParameterSetName (Default)</span></span>
```
Add-AzAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53792-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="53792-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53792-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="53792-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53792-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53792-108">DESCRIPTION</span></span>
<span data-ttu-id="53792-109">Das Add-AzAnalysisServicesAccount cmdlet wird verwendet, um sich bei einer Instanz des Azure Analysis Services Server anzumelden.</span><span class="sxs-lookup"><span data-stu-id="53792-109">The Add-AzAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="53792-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="53792-110">EXAMPLES</span></span>

### <span data-ttu-id="53792-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="53792-111">Example 1</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="53792-112">In diesem Beispiel wird das von der Variablen "$UserCredential" angegebene Konto der westcentralus.asazure.windows.net Analysis Services-Umgebung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="53792-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="53792-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="53792-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="53792-114">Der erste Befehl ruft die Anmeldeinformationen für den Anwendungsdienstprinzipal ab und speichert sie dann in der $ApplicationCredential Variable.</span><span class="sxs-lookup"><span data-stu-id="53792-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="53792-115">Mit dem zweiten Befehl wird das Anwendungsdienstprinzipalkonto, das von der Variablen "$ApplicationCredential" und "TenantId" angegeben wird, der westcentralus.asazure.windows.net Analysis Services-Umgebung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="53792-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="53792-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="53792-116">Example 3</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="53792-117">In diesem Beispiel wird das Anwendungsdienstprinzipalkonto, das durch "ApplicationId", "TenantId" und "CertificateThumbprint" angegeben ist, der westcentralus.asazure.windows.net Analysis Services-Umgebung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="53792-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="53792-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53792-118">PARAMETERS</span></span>

### <span data-ttu-id="53792-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="53792-119">-ApplicationId</span></span>
<span data-ttu-id="53792-120">Die Anwendungs-ID.</span><span class="sxs-lookup"><span data-stu-id="53792-120">The application ID.</span></span>

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

### <span data-ttu-id="53792-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="53792-121">-CertificateThumbprint</span></span>
<span data-ttu-id="53792-122">Zertifikathash (Thumbprint)</span><span class="sxs-lookup"><span data-stu-id="53792-122">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="53792-123">-Credential</span><span class="sxs-lookup"><span data-stu-id="53792-123">-Credential</span></span>
<span data-ttu-id="53792-124">Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="53792-124">Login credentials</span></span>

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

### <span data-ttu-id="53792-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="53792-125">-RolloutEnvironment</span></span>
<span data-ttu-id="53792-126">Name der Azure Analysis Services-Umgebung, bei der sie sich anmeldet.</span><span class="sxs-lookup"><span data-stu-id="53792-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="53792-127">Bei dem vollständigen Namen des Servers , beispielsweise asazure://westcentralus.asazure.windows.net/testserver, wird der richtige Wert für diese Variable westcentralus.asazure.windows.net</span><span class="sxs-lookup"><span data-stu-id="53792-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

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

### <span data-ttu-id="53792-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="53792-128">-ServicePrincipal</span></span>
<span data-ttu-id="53792-129">Gibt an, dass sich dieses Konto authentifiziert, indem Anmeldeinformationen für den Dienstprinzipal angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="53792-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="53792-130">-TenantId</span><span class="sxs-lookup"><span data-stu-id="53792-130">-TenantId</span></span>
<span data-ttu-id="53792-131">Name oder ID des Mandanten</span><span class="sxs-lookup"><span data-stu-id="53792-131">Tenant name or ID</span></span>

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

### <span data-ttu-id="53792-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53792-132">-Confirm</span></span>
<span data-ttu-id="53792-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="53792-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53792-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="53792-134">-WhatIf</span></span>
<span data-ttu-id="53792-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="53792-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53792-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="53792-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53792-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53792-137">CommonParameters</span></span>
<span data-ttu-id="53792-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53792-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53792-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53792-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53792-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="53792-140">INPUTS</span></span>

### <span data-ttu-id="53792-141">Keine</span><span class="sxs-lookup"><span data-stu-id="53792-141">None</span></span>

## <span data-ttu-id="53792-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="53792-142">OUTPUTS</span></span>

### <span data-ttu-id="53792-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="53792-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="53792-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="53792-144">NOTES</span></span>
<span data-ttu-id="53792-145">Alias: Login-AzAsAccount</span><span class="sxs-lookup"><span data-stu-id="53792-145">Alias: Login-AzAsAccount</span></span>

## <span data-ttu-id="53792-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="53792-146">RELATED LINKS</span></span>
