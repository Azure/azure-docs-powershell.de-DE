---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: 44091f612720851a0ab13d54716f441d73a04065
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943510"
---
# <span data-ttu-id="188f9-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="188f9-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="188f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="188f9-102">SYNOPSIS</span></span>
<span data-ttu-id="188f9-103">Aktualisiert einen vorhandenen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="188f9-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="188f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="188f9-104">SYNTAX</span></span>

### <span data-ttu-id="188f9-105">SpObjectIdWithDisplayNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="188f9-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="188f9-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="188f9-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="188f9-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="188f9-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="188f9-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="188f9-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="188f9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="188f9-109">DESCRIPTION</span></span>
<span data-ttu-id="188f9-110">Aktualisiert einen vorhandenen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="188f9-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="188f9-111">Zum Aktualisieren der Anmeldeinformationen, die diesem Dienstprinzipal zugeordnet sind, verwenden Sie bitte New-AzADSpCredential Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="188f9-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="188f9-112">Verwenden Sie zum Aktualisieren der Eigenschaften, die der zugrunde liegenden Anwendung zugeordnet sind, Update-AzADApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="188f9-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="188f9-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="188f9-113">EXAMPLES</span></span>

### <span data-ttu-id="188f9-114">Beispiel 1: Aktualisieren des Anzeigenamens eines Dienstprinzipals</span><span class="sxs-lookup"><span data-stu-id="188f9-114">Example 1: Update the display name of a service principal</span></span>

```powershell
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="188f9-115">Aktualisiert den Anzeigenamen des Dienstprinzipals mit der Objekt-ID '784136ca-3ae2-4fdd-a388-89d793e7c780' in "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="188f9-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="188f9-116">Beispiel 2: Aktualisieren des Anzeigenamens eines Dienstprinzipals mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="188f9-116">Example 2: Update the display name of a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="188f9-117">Ruft den Dienstprinzipal mit der Objekt-ID '784136ca-3ae2-4fdd-a388-89d793e7c780' ab und gibt diese an das Update-AzADServicePrincipal-Cmdlet weiter, um den Anzeigenamen des Dienstprinzipals auf "MyNewDisplayName" zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="188f9-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

### <span data-ttu-id="188f9-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="188f9-118">Example 3</span></span>

<span data-ttu-id="188f9-119">Aktualisiert einen vorhandenen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="188f9-119">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="188f9-120">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="188f9-120">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzADServicePrincipal -IdentifierUri https://mySecretApp1 -ObjectId 00000000-0000-0000-0000-00000000000000000
```

## <span data-ttu-id="188f9-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="188f9-121">PARAMETERS</span></span>

### <span data-ttu-id="188f9-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="188f9-122">-ApplicationId</span></span>
<span data-ttu-id="188f9-123">Die Anwendungs-ID des zu aktualisierende Dienstprinzipals.</span><span class="sxs-lookup"><span data-stu-id="188f9-123">The application id of the service principal to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpApplicationIdWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="188f9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="188f9-124">-DefaultProfile</span></span>
<span data-ttu-id="188f9-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="188f9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="188f9-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="188f9-126">-DisplayName</span></span>
<span data-ttu-id="188f9-127">Der Anzeigename für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="188f9-127">The display name for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet, SPNWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="188f9-128">-Homepage</span><span class="sxs-lookup"><span data-stu-id="188f9-128">-Homepage</span></span>
<span data-ttu-id="188f9-129">Die Homepage für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="188f9-129">The homepage for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="188f9-130">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="188f9-130">-IdentifierUri</span></span>
<span data-ttu-id="188f9-131">Die URI(n) des Bezeichners für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="188f9-131">The identifier URI(s) for the service principal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="188f9-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="188f9-132">-InputObject</span></span>
<span data-ttu-id="188f9-133">Das Objekt, das den zu aktualisierenden Dienstprinzipal darstellt.</span><span class="sxs-lookup"><span data-stu-id="188f9-133">The object representing the service principal to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="188f9-134">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="188f9-134">-KeyCredential</span></span>
<span data-ttu-id="188f9-135">Die Schlüsselanmeldeinformationen für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="188f9-135">The key credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.KeyCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="188f9-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="188f9-136">-ObjectId</span></span>
<span data-ttu-id="188f9-137">Die Objekt-ID des zu aktualisierende Dienstprinzipals.</span><span class="sxs-lookup"><span data-stu-id="188f9-137">The object id of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="188f9-138">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="188f9-138">-PasswordCredential</span></span>
<span data-ttu-id="188f9-139">Die Kennwortanmeldeinformationen für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="188f9-139">The password credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.PasswordCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="188f9-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="188f9-140">-ServicePrincipalName</span></span>
<span data-ttu-id="188f9-141">Der SPN des zu aktualisierende Dienstprinzipals.</span><span class="sxs-lookup"><span data-stu-id="188f9-141">The SPN of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="188f9-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="188f9-142">-Confirm</span></span>
<span data-ttu-id="188f9-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="188f9-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="188f9-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="188f9-144">-WhatIf</span></span>
<span data-ttu-id="188f9-145">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="188f9-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="188f9-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="188f9-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="188f9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="188f9-147">CommonParameters</span></span>
<span data-ttu-id="188f9-148">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="188f9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="188f9-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="188f9-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="188f9-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="188f9-150">INPUTS</span></span>

### <span data-ttu-id="188f9-151">System.String</span><span class="sxs-lookup"><span data-stu-id="188f9-151">System.String</span></span>

### <span data-ttu-id="188f9-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="188f9-152">System.Guid</span></span>

### <span data-ttu-id="188f9-153">Microsoft.Azure.Commands.ActiveDirectory.PSDServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="188f9-153">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="188f9-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="188f9-154">OUTPUTS</span></span>

### <span data-ttu-id="188f9-155">Microsoft.Azure.Commands.ActiveDirectory.PSDServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="188f9-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="188f9-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="188f9-156">NOTES</span></span>

## <span data-ttu-id="188f9-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="188f9-157">RELATED LINKS</span></span>