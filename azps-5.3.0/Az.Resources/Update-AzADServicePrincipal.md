---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: 05bd5f7997c83c2be6b50faf0e6d88ee7413a773
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375750"
---
# <span data-ttu-id="c8eef-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c8eef-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="c8eef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8eef-102">SYNOPSIS</span></span>
<span data-ttu-id="c8eef-103">Aktualisiert einen vorhandenen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="c8eef-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="c8eef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8eef-104">SYNTAX</span></span>

### <span data-ttu-id="c8eef-105">SpObjectIdWithDisplayNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c8eef-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8eef-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8eef-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8eef-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8eef-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8eef-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8eef-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8eef-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8eef-109">DESCRIPTION</span></span>
<span data-ttu-id="c8eef-110">Aktualisiert einen vorhandenen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="c8eef-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="c8eef-111">Zum Aktualisieren der Anmeldeinformationen, die diesem Dienstprinzipal zugeordnet sind, verwenden Sie New-AzADSpCredential Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8eef-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="c8eef-112">Um die Eigenschaften zu aktualisieren, die der zugrunde liegenden Anwendung zugeordnet sind, verwenden Sie Update-AzADApplication Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8eef-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="c8eef-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c8eef-113">EXAMPLES</span></span>

### <span data-ttu-id="c8eef-114">Beispiel 1: Aktualisieren des Anzeigenamens eines Dienstprinzipal</span><span class="sxs-lookup"><span data-stu-id="c8eef-114">Example 1: Update the display name of a service principal</span></span>

```powershell
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="c8eef-115">Aktualisiert den Anzeigenamen des Dienstprinzipal mit der Objekt-ID '784136ca-3ae2-4fdd-a388-89d793e7c780' in 'MyNewDisplayName'.</span><span class="sxs-lookup"><span data-stu-id="c8eef-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="c8eef-116">Beispiel 2: Aktualisieren des Anzeigenamens eines Dienstprinzipal mithilfe der Piping</span><span class="sxs-lookup"><span data-stu-id="c8eef-116">Example 2: Update the display name of a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="c8eef-117">Ruft den Dienstprinzipal mit der Objekt-ID '784136ca-3ae2-4fdd-a388-89d793e7c780' ab und gibt diese an das cmdlet Update-AzADServicePrincipal weiter, um den Anzeigenamen des Dienstprinzipals auf "MyNewDisplayName" zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c8eef-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

### <span data-ttu-id="c8eef-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c8eef-118">Example 3</span></span>

<span data-ttu-id="c8eef-119">Aktualisiert einen vorhandenen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="c8eef-119">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="c8eef-120">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="c8eef-120">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzADServicePrincipal -IdentifierUri https://mySecretApp1 -ObjectId 00000000-0000-0000-0000-00000000000000000
```

## <span data-ttu-id="c8eef-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8eef-121">PARAMETERS</span></span>

### <span data-ttu-id="c8eef-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c8eef-122">-ApplicationId</span></span>
<span data-ttu-id="c8eef-123">Die Anwendungs-ID des Dienstprinzipal, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8eef-123">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="c8eef-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8eef-124">-DefaultProfile</span></span>
<span data-ttu-id="c8eef-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8eef-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8eef-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c8eef-126">-DisplayName</span></span>
<span data-ttu-id="c8eef-127">Der Anzeigename für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="c8eef-127">The display name for the service principal.</span></span>

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

### <span data-ttu-id="c8eef-128">-Homepage</span><span class="sxs-lookup"><span data-stu-id="c8eef-128">-Homepage</span></span>
<span data-ttu-id="c8eef-129">Die Startseite für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="c8eef-129">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="c8eef-130">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="c8eef-130">-IdentifierUri</span></span>
<span data-ttu-id="c8eef-131">Die Bezeichner-URI(n) für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="c8eef-131">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="c8eef-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8eef-132">-InputObject</span></span>
<span data-ttu-id="c8eef-133">Das Objekt, das den zu aktualisierenden Dienstprinzipal darstellt.</span><span class="sxs-lookup"><span data-stu-id="c8eef-133">The object representing the service principal to update.</span></span>

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

### <span data-ttu-id="c8eef-134">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="c8eef-134">-KeyCredential</span></span>
<span data-ttu-id="c8eef-135">Die Schlüsselanmeldeinformationen für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="c8eef-135">The key credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="c8eef-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c8eef-136">-ObjectId</span></span>
<span data-ttu-id="c8eef-137">Die Objekt-ID des Dienstprinzipal, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8eef-137">The object id of the service principal to update.</span></span>

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

### <span data-ttu-id="c8eef-138">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="c8eef-138">-PasswordCredential</span></span>
<span data-ttu-id="c8eef-139">Die Kennwortanmeldeinformationen für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="c8eef-139">The password credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="c8eef-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c8eef-140">-ServicePrincipalName</span></span>
<span data-ttu-id="c8eef-141">Der SPN des Dienstprinzipal, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8eef-141">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="c8eef-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8eef-142">-Confirm</span></span>
<span data-ttu-id="c8eef-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8eef-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8eef-144">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c8eef-144">-WhatIf</span></span>
<span data-ttu-id="c8eef-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8eef-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8eef-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8eef-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8eef-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8eef-147">CommonParameters</span></span>
<span data-ttu-id="c8eef-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8eef-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8eef-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8eef-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8eef-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c8eef-150">INPUTS</span></span>

### <span data-ttu-id="c8eef-151">System.String</span><span class="sxs-lookup"><span data-stu-id="c8eef-151">System.String</span></span>

### <span data-ttu-id="c8eef-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="c8eef-152">System.Guid</span></span>

### <span data-ttu-id="c8eef-153">Microsoft.Azure.Commands.ActiveDirectory.WAHLDServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c8eef-153">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="c8eef-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c8eef-154">OUTPUTS</span></span>

### <span data-ttu-id="c8eef-155">Microsoft.Azure.Commands.ActiveDirectory.WAHLDServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c8eef-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="c8eef-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c8eef-156">NOTES</span></span>

## <span data-ttu-id="c8eef-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c8eef-157">RELATED LINKS</span></span>