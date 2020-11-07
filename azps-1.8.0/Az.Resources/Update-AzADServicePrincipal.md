---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: e4fafb6c1ddc4dda05b6536501f713d04c312172
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659498"
---
# <span data-ttu-id="fdfc0-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="fdfc0-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="fdfc0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fdfc0-102">SYNOPSIS</span></span>
<span data-ttu-id="fdfc0-103">Aktualisiert einen vorhandenen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="fdfc0-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="fdfc0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdfc0-104">SYNTAX</span></span>

### <span data-ttu-id="fdfc0-105">SpObjectIdWithDisplayNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fdfc0-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdfc0-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdfc0-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdfc0-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdfc0-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdfc0-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdfc0-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdfc0-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fdfc0-109">DESCRIPTION</span></span>
<span data-ttu-id="fdfc0-110">Aktualisiert einen vorhandenen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="fdfc0-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="fdfc0-111">Verwenden Sie New-AzADSpCredential-Cmdlet, um die dem Dienstprinzipal zugeordneten Anmeldeinformationen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="fdfc0-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="fdfc0-112">Verwenden Sie Update-AzADApplication-Cmdlet, um die Eigenschaften zu aktualisieren, die der zugrunde liegenden Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fdfc0-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="fdfc0-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdfc0-113">EXAMPLES</span></span>

### <span data-ttu-id="fdfc0-114">Beispiel 1 – Aktualisieren des Anzeigenamens eines Dienst Prinzipals</span><span class="sxs-lookup"><span data-stu-id="fdfc0-114">Example 1 - Update the display name of a service principal</span></span>

```
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="fdfc0-115">Aktualisiert den Anzeigenamen des Dienst Prinzipals mit der Objekt-ID "784136ca-3ae2-4fdd-A388-89d793e7c780" als "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="fdfc0-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="fdfc0-116">Beispiel 2 – Aktualisieren des Anzeigenamens eines Dienst Prinzipals mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="fdfc0-116">Example 2 - Update the display name of a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="fdfc0-117">Ruft den Dienstprinzipal mit der Objekt-ID "784136ca-3ae2-4fdd-A388-89d793e7c780" und Pipes ab, die zum Cmdlet Update-AzADServicePrincipal, um den Anzeigenamen des Dienst Prinzipals auf "MyNewDisplayName" zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="fdfc0-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

## <span data-ttu-id="fdfc0-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdfc0-118">PARAMETERS</span></span>

### <span data-ttu-id="fdfc0-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="fdfc0-119">-ApplicationId</span></span>
<span data-ttu-id="fdfc0-120">Die Anwendungs-ID des Dienst Prinzipals, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fdfc0-120">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="fdfc0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdfc0-121">-DefaultProfile</span></span>
<span data-ttu-id="fdfc0-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fdfc0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdfc0-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fdfc0-123">-DisplayName</span></span>
<span data-ttu-id="fdfc0-124">Der Anzeigename für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="fdfc0-124">The display name for the service principal.</span></span>

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

### <span data-ttu-id="fdfc0-125">-Startseite</span><span class="sxs-lookup"><span data-stu-id="fdfc0-125">-Homepage</span></span>
<span data-ttu-id="fdfc0-126">Die Homepage des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="fdfc0-126">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="fdfc0-127">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="fdfc0-127">-IdentifierUri</span></span>
<span data-ttu-id="fdfc0-128">Die Identifier-URI (s) für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="fdfc0-128">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="fdfc0-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fdfc0-129">-InputObject</span></span>
<span data-ttu-id="fdfc0-130">Das Objekt, das den zu aktualisierbaren Dienstprinzipal darstellt.</span><span class="sxs-lookup"><span data-stu-id="fdfc0-130">The object representing the service principal to update.</span></span>

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

### <span data-ttu-id="fdfc0-131">-Keycredential</span><span class="sxs-lookup"><span data-stu-id="fdfc0-131">-KeyCredential</span></span>
<span data-ttu-id="fdfc0-132">Die Schlüssel Anmeldeinformationen für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="fdfc0-132">The key credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="fdfc0-133">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="fdfc0-133">-ObjectId</span></span>
<span data-ttu-id="fdfc0-134">Die Objekt-ID des Dienst Prinzipals, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fdfc0-134">The object id of the service principal to update.</span></span>

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

### <span data-ttu-id="fdfc0-135">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="fdfc0-135">-PasswordCredential</span></span>
<span data-ttu-id="fdfc0-136">Die Kennwortanmeldeinformationen für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="fdfc0-136">The password credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="fdfc0-137">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fdfc0-137">-ServicePrincipalName</span></span>
<span data-ttu-id="fdfc0-138">Der SPN des Dienst Prinzipals, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fdfc0-138">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="fdfc0-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fdfc0-139">-Confirm</span></span>
<span data-ttu-id="fdfc0-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fdfc0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdfc0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdfc0-141">-WhatIf</span></span>
<span data-ttu-id="fdfc0-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fdfc0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdfc0-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fdfc0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdfc0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdfc0-144">CommonParameters</span></span>
<span data-ttu-id="fdfc0-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdfc0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdfc0-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdfc0-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdfc0-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fdfc0-147">INPUTS</span></span>

### <span data-ttu-id="fdfc0-148">System. String</span><span class="sxs-lookup"><span data-stu-id="fdfc0-148">System.String</span></span>

### <span data-ttu-id="fdfc0-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="fdfc0-149">System.Guid</span></span>

### <span data-ttu-id="fdfc0-150">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="fdfc0-150">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="fdfc0-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fdfc0-151">OUTPUTS</span></span>

### <span data-ttu-id="fdfc0-152">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="fdfc0-152">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="fdfc0-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="fdfc0-153">NOTES</span></span>

## <span data-ttu-id="fdfc0-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fdfc0-154">RELATED LINKS</span></span>
