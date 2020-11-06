---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmADServicePrincipal.md
ms.openlocfilehash: ce778da76b0dfc81a8438bdd0fdc3e0a20215843
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505274"
---
# <span data-ttu-id="559cd-101">Update-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="559cd-101">Update-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="559cd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="559cd-102">SYNOPSIS</span></span>
<span data-ttu-id="559cd-103">Aktualisiert einen vorhandenen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="559cd-103">Updates an existing azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="559cd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="559cd-104">SYNTAX</span></span>

### <span data-ttu-id="559cd-105">SpObjectIdWithDisplayNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="559cd-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzureRmADServicePrincipal -ObjectId <Guid> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="559cd-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="559cd-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzureRmADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="559cd-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="559cd-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="559cd-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="559cd-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzureRmADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>]
 [-Homepage <String>] [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>]
 [-PasswordCredential <PasswordCredential[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="559cd-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="559cd-109">DESCRIPTION</span></span>
<span data-ttu-id="559cd-110">Aktualisiert einen vorhandenen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="559cd-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="559cd-111">Verwenden Sie New-AzureRmADSpCredential-Cmdlet, um die dem Dienstprinzipal zugeordneten Anmeldeinformationen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="559cd-111">To update the credentials associated with this service principal, please use New-AzureRmADSpCredential cmdlet.</span></span> <span data-ttu-id="559cd-112">Verwenden Sie Update-AzureRmADApplication-Cmdlet, um die Eigenschaften zu aktualisieren, die der zugrunde liegenden Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="559cd-112">To update the properties associated with the underlying application, please use Update-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="559cd-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="559cd-113">EXAMPLES</span></span>

### <span data-ttu-id="559cd-114">Beispiel 1 – Aktualisieren des Anzeigenamens eines Dienst Prinzipals</span><span class="sxs-lookup"><span data-stu-id="559cd-114">Example 1 - Update the display name of a service principal</span></span>

```
PS C:\> Update-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="559cd-115">Aktualisiert den Anzeigenamen des Dienst Prinzipals mit der Objekt-ID "784136ca-3ae2-4fdd-A388-89d793e7c780" als "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="559cd-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="559cd-116">Beispiel 2 – Aktualisieren des Anzeigenamens eines Dienst Prinzipals mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="559cd-116">Example 2 - Update the display name of a service principal using piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzureRmADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="559cd-117">Ruft den Dienstprinzipal mit der Objekt-ID "784136ca-3ae2-4fdd-A388-89d793e7c780" und Pipes ab, die zum Cmdlet Update-AzureRmADServicePrincipal, um den Anzeigenamen des Dienst Prinzipals auf "MyNewDisplayName" zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="559cd-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzureRmADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

## <span data-ttu-id="559cd-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="559cd-118">PARAMETERS</span></span>

### <span data-ttu-id="559cd-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="559cd-119">-ApplicationId</span></span>
<span data-ttu-id="559cd-120">Die Anwendungs-ID des Dienst Prinzipals, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="559cd-120">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="559cd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="559cd-121">-DefaultProfile</span></span>
<span data-ttu-id="559cd-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="559cd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="559cd-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="559cd-123">-DisplayName</span></span>
<span data-ttu-id="559cd-124">Der Anzeigename für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="559cd-124">The display name for the service principal.</span></span>

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

### <span data-ttu-id="559cd-125">-Startseite</span><span class="sxs-lookup"><span data-stu-id="559cd-125">-Homepage</span></span>
<span data-ttu-id="559cd-126">Die Homepage des Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="559cd-126">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="559cd-127">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="559cd-127">-IdentifierUri</span></span>
<span data-ttu-id="559cd-128">Die Identifier-URI (s) für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="559cd-128">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="559cd-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="559cd-129">-InputObject</span></span>
<span data-ttu-id="559cd-130">Das Objekt, das den zu aktualisierbaren Dienstprinzipal darstellt.</span><span class="sxs-lookup"><span data-stu-id="559cd-130">The object representing the service principal to update.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="559cd-131">-Keycredential</span><span class="sxs-lookup"><span data-stu-id="559cd-131">-KeyCredential</span></span>
<span data-ttu-id="559cd-132">Die Schlüssel Anmeldeinformationen für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="559cd-132">The key credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.Models.KeyCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="559cd-133">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="559cd-133">-ObjectId</span></span>
<span data-ttu-id="559cd-134">Die Objekt-ID des Dienst Prinzipals, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="559cd-134">The object id of the service principal to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="559cd-135">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="559cd-135">-PasswordCredential</span></span>
<span data-ttu-id="559cd-136">Die Kennwortanmeldeinformationen für den Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="559cd-136">The password credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.Models.PasswordCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="559cd-137">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="559cd-137">-ServicePrincipalName</span></span>
<span data-ttu-id="559cd-138">Der SPN des Dienst Prinzipals, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="559cd-138">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="559cd-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="559cd-139">-Confirm</span></span>
<span data-ttu-id="559cd-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="559cd-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="559cd-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="559cd-141">-WhatIf</span></span>
<span data-ttu-id="559cd-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="559cd-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="559cd-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="559cd-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="559cd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="559cd-144">CommonParameters</span></span>
<span data-ttu-id="559cd-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="559cd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="559cd-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="559cd-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="559cd-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="559cd-147">INPUTS</span></span>

### <span data-ttu-id="559cd-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="559cd-148">System.Guid</span></span>

### <span data-ttu-id="559cd-149">System. String</span><span class="sxs-lookup"><span data-stu-id="559cd-149">System.String</span></span>

### <span data-ttu-id="559cd-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="559cd-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="559cd-151">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="559cd-151">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="559cd-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="559cd-152">OUTPUTS</span></span>

### <span data-ttu-id="559cd-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="559cd-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="559cd-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="559cd-154">NOTES</span></span>

## <span data-ttu-id="559cd-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="559cd-155">RELATED LINKS</span></span>
