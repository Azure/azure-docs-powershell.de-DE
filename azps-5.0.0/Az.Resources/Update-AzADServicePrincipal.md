---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: 05bd5f7997c83c2be6b50faf0e6d88ee7413a773
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302446"
---
# <span data-ttu-id="bdede-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bdede-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="bdede-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bdede-102">SYNOPSIS</span></span>
<span data-ttu-id="bdede-103">Aktualisiert einen vorhandenen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="bdede-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="bdede-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdede-104">SYNTAX</span></span>

### <span data-ttu-id="bdede-105">SpObjectIdWithDisplayNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bdede-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdede-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdede-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdede-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdede-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdede-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdede-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdede-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bdede-109">DESCRIPTION</span></span>
<span data-ttu-id="bdede-110">Aktualisiert einen vorhandenen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="bdede-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="bdede-111">Verwenden Sie New-AzADSpCredential-Cmdlet, um die dem Dienstprinzipal zugeordneten Anmeldeinformationen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="bdede-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="bdede-112">Verwenden Sie Update-AzADApplication-Cmdlet, um die Eigenschaften zu aktualisieren, die der zugrunde liegenden Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bdede-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="bdede-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bdede-113">EXAMPLES</span></span>

### <span data-ttu-id="bdede-114">Beispiel 1: Aktualisieren des Anzeigenamens eines Dienst Prinzipals</span><span class="sxs-lookup"><span data-stu-id="bdede-114">Example 1: Update the display name of a service principal</span></span>

```powershell
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="bdede-115">Aktualisiert den Anzeigenamen des Dienst Prinzipals mit der Objekt-ID "784136ca-3ae2-4fdd-A388-89d793e7c780" als "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="bdede-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="bdede-116">Beispiel 2: Aktualisieren des Anzeigenamens eines Dienst Prinzipals mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="bdede-116">Example 2: Update the display name of a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="bdede-117">Ruft den Dienstprinzipal mit der Objekt-ID "784136ca-3ae2-4fdd-A388-89d793e7c780" und Pipes ab, die zum Cmdlet Update-AzADServicePrincipal, um den Anzeigenamen des Dienst Prinzipals auf "MyNewDisplayName" zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="bdede-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

### <span data-ttu-id="bdede-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="bdede-118">Example 3</span></span>

<span data-ttu-id="bdede-119">Aktualisiert einen vorhandenen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="bdede-119">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="bdede-120">automatisch</span><span class="sxs-lookup"><span data-stu-id="bdede-120">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzADServicePrincipal -IdentifierUri https://mySecretApp1 -ObjectId 00000000-0000-0000-0000-00000000000000000
```

## <span data-ttu-id="bdede-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdede-121">PARAMETERS</span></span>

### <span data-ttu-id="bdede-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="bdede-122">-ApplicationId</span></span>
<span data-ttu-id="bdede-123">Die Anwendungs-ID des Dienst Prinzipals, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bdede-123">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="bdede-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdede-124">-DefaultProfile</span></span>
<span data-ttu-id="bdede-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bdede-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdede-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bdede-126">-DisplayName</span></span>
<span data-ttu-id="bdede-127">Der Anzeigename für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="bdede-127">The display name for the service principal.</span></span>

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

### <span data-ttu-id="bdede-128">-Startseite</span><span class="sxs-lookup"><span data-stu-id="bdede-128">-Homepage</span></span>
<span data-ttu-id="bdede-129">Die Homepage des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="bdede-129">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="bdede-130">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="bdede-130">-IdentifierUri</span></span>
<span data-ttu-id="bdede-131">Die Identifier-URI (s) für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="bdede-131">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="bdede-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bdede-132">-InputObject</span></span>
<span data-ttu-id="bdede-133">Das Objekt, das den zu aktualisierbaren Dienstprinzipal darstellt.</span><span class="sxs-lookup"><span data-stu-id="bdede-133">The object representing the service principal to update.</span></span>

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

### <span data-ttu-id="bdede-134">-Keycredential</span><span class="sxs-lookup"><span data-stu-id="bdede-134">-KeyCredential</span></span>
<span data-ttu-id="bdede-135">Die Schlüssel Anmeldeinformationen für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="bdede-135">The key credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="bdede-136">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="bdede-136">-ObjectId</span></span>
<span data-ttu-id="bdede-137">Die Objekt-ID des Dienst Prinzipals, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bdede-137">The object id of the service principal to update.</span></span>

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

### <span data-ttu-id="bdede-138">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="bdede-138">-PasswordCredential</span></span>
<span data-ttu-id="bdede-139">Die Kennwortanmeldeinformationen für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="bdede-139">The password credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="bdede-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="bdede-140">-ServicePrincipalName</span></span>
<span data-ttu-id="bdede-141">Der SPN des Dienst Prinzipals, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bdede-141">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="bdede-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bdede-142">-Confirm</span></span>
<span data-ttu-id="bdede-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bdede-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdede-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdede-144">-WhatIf</span></span>
<span data-ttu-id="bdede-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bdede-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdede-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bdede-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdede-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdede-147">CommonParameters</span></span>
<span data-ttu-id="bdede-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdede-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdede-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdede-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdede-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bdede-150">INPUTS</span></span>

### <span data-ttu-id="bdede-151">System. String</span><span class="sxs-lookup"><span data-stu-id="bdede-151">System.String</span></span>

### <span data-ttu-id="bdede-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="bdede-152">System.Guid</span></span>

### <span data-ttu-id="bdede-153">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bdede-153">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="bdede-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bdede-154">OUTPUTS</span></span>

### <span data-ttu-id="bdede-155">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bdede-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="bdede-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="bdede-156">NOTES</span></span>

## <span data-ttu-id="bdede-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bdede-157">RELATED LINKS</span></span>