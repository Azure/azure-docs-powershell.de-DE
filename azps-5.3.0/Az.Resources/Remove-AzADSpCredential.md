---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: bcb33f87b85eb6ad5bce9ba812ebccb4d154e920
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459232"
---
# <span data-ttu-id="7aaf7-101">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="7aaf7-101">Remove-AzADSpCredential</span></span>

## <span data-ttu-id="7aaf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7aaf7-102">SYNOPSIS</span></span>
<span data-ttu-id="7aaf7-103">Entfernt anmeldeinformationen aus einem Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="7aaf7-103">Removes a credential from a service principal.</span></span>

## <span data-ttu-id="7aaf7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7aaf7-104">SYNTAX</span></span>

### <span data-ttu-id="7aaf7-105">ObjectIdWithKeyIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7aaf7-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADSpCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7aaf7-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7aaf7-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7aaf7-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7aaf7-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7aaf7-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7aaf7-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7aaf7-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7aaf7-109">DESCRIPTION</span></span>
<span data-ttu-id="7aaf7-110">Das Remove-AzADSpCredential cmdlet kann verwendet werden, um im Falle eines Kompromisses oder als Teil des Ablaufs des Anmeldeinformationsschlüsselrollovers einen Anmeldeinformationsschlüssel aus einem Dienstprinzipal zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="7aaf7-110">The Remove-AzADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="7aaf7-111">Der Dienstprinzipal wird durch Angabe der Objekt-ID oder des Dienstprinzipalnamens (Service Principal Name, SPN) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7aaf7-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="7aaf7-112">Die zu entfernenden Anmeldeinformationen werden durch ihre Schlüssel-ID identifiziert, wenn einzelne Anmeldeinformationen entfernt werden sollen, oder durch einen Schalter "Alle", um alle Anmeldeinformationen zu löschen, die dem Dienstprinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7aaf7-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="7aaf7-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7aaf7-113">EXAMPLES</span></span>

### <span data-ttu-id="7aaf7-114">Beispiel 1: Entfernen bestimmter Anmeldeinformationen aus einem Dienstprinzipal</span><span class="sxs-lookup"><span data-stu-id="7aaf7-114">Example 1: Remove a specific credential from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="7aaf7-115">Entfernt die Anmeldeinformationen mit der Schlüssel-ID '9044423a-60a3-45ac-9ab1-09534157ebb' aus dem Dienstprinzipal mit der Objekt-ID '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span><span class="sxs-lookup"><span data-stu-id="7aaf7-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="7aaf7-116">Beispiel 2: Entfernen aller Anmeldeinformationen aus einem Dienstprinzipal</span><span class="sxs-lookup"><span data-stu-id="7aaf7-116">Example 2: Remove all credentials from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="7aaf7-117">Entfernt alle Anmeldeinformationen aus dem Dienstprinzipal mit dem SPN " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="7aaf7-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="7aaf7-118">Beispiel 3: Entfernen aller Anmeldeinformationen von einem Dienstprinzipal mithilfe der Piping</span><span class="sxs-lookup"><span data-stu-id="7aaf7-118">Example 3: Remove all credentials from a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

<span data-ttu-id="7aaf7-119">Ruft den Dienstprinzipal mit der Objekt-ID '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' ab und gibt diese an das cmdlet Remove-AzADSpCredential weiter, um alle Anmeldeinformationen von diesem Dienstprinzipal zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="7aaf7-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="7aaf7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7aaf7-120">PARAMETERS</span></span>

### <span data-ttu-id="7aaf7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aaf7-121">-DefaultProfile</span></span>
<span data-ttu-id="7aaf7-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7aaf7-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7aaf7-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7aaf7-123">-DisplayName</span></span>
<span data-ttu-id="7aaf7-124">Der Anzeigename des Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="7aaf7-124">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aaf7-125">-Force</span><span class="sxs-lookup"><span data-stu-id="7aaf7-125">-Force</span></span>
<span data-ttu-id="7aaf7-126">Wechseln Sie zum Löschen von Anmeldeinformationen ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="7aaf7-126">Switch to delete credential without a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aaf7-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="7aaf7-127">-KeyId</span></span>
<span data-ttu-id="7aaf7-128">Gibt den zu entfernenden Anmeldeinformationsschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="7aaf7-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="7aaf7-129">Die Schlüssel-IDs für einen Dienstprinzipal können mit dem cmdlet Get-AzADSpCredential ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="7aaf7-129">The key Ids for a service principal can be obtained using the Get-AzADSpCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet, ServicePrincipalObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aaf7-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7aaf7-130">-ObjectId</span></span>
<span data-ttu-id="7aaf7-131">Die Objekt-ID des Dienstprinzipal, aus dem die Anmeldeinformationen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="7aaf7-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aaf7-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7aaf7-132">-PassThru</span></span>
<span data-ttu-id="7aaf7-133">Wenn Sie diese Angabe angeben, wird "true" zurückgeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="7aaf7-133">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aaf7-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="7aaf7-134">-ServicePrincipalName</span></span>
<span data-ttu-id="7aaf7-135">Der Name (SPN) des Dienstprinzipal, aus dem die Anmeldeinformationen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="7aaf7-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aaf7-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="7aaf7-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="7aaf7-137">Das Dienstprinzipalobjekt, aus dem die Anmeldeinformationen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="7aaf7-137">The service principal object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7aaf7-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7aaf7-138">-Confirm</span></span>
<span data-ttu-id="7aaf7-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7aaf7-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7aaf7-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7aaf7-140">-WhatIf</span></span>
<span data-ttu-id="7aaf7-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7aaf7-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7aaf7-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7aaf7-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7aaf7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aaf7-143">CommonParameters</span></span>
<span data-ttu-id="7aaf7-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7aaf7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aaf7-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7aaf7-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aaf7-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7aaf7-146">INPUTS</span></span>

### <span data-ttu-id="7aaf7-147">System.String</span><span class="sxs-lookup"><span data-stu-id="7aaf7-147">System.String</span></span>

### <span data-ttu-id="7aaf7-148">Microsoft.Azure.Commands.ActiveDirectory.WAHLDServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7aaf7-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="7aaf7-149">System.Guid</span><span class="sxs-lookup"><span data-stu-id="7aaf7-149">System.Guid</span></span>

## <span data-ttu-id="7aaf7-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7aaf7-150">OUTPUTS</span></span>

### <span data-ttu-id="7aaf7-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7aaf7-151">System.Boolean</span></span>

## <span data-ttu-id="7aaf7-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7aaf7-152">NOTES</span></span>

## <span data-ttu-id="7aaf7-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7aaf7-153">RELATED LINKS</span></span>

[<span data-ttu-id="7aaf7-154">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="7aaf7-154">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="7aaf7-155">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="7aaf7-155">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="7aaf7-156">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7aaf7-156">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

