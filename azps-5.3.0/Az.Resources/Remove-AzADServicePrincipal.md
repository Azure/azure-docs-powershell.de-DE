---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: 7f306503754ca945ab4abb001cf08f8574b67025
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459231"
---
# <span data-ttu-id="65846-101">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="65846-101">Remove-AzADServicePrincipal</span></span>

## <span data-ttu-id="65846-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65846-102">SYNOPSIS</span></span>
<span data-ttu-id="65846-103">Löscht den Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="65846-103">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="65846-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65846-104">SYNTAX</span></span>

### <span data-ttu-id="65846-105">ObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="65846-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADServicePrincipal -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65846-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65846-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65846-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="65846-107">SPNParameterSet</span></span>
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65846-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="65846-108">DisplayNameParameterSet</span></span>
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65846-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65846-109">InputObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65846-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65846-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65846-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65846-111">DESCRIPTION</span></span>
<span data-ttu-id="65846-112">Löscht den Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="65846-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="65846-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="65846-113">EXAMPLES</span></span>

### <span data-ttu-id="65846-114">Beispiel 1: Entfernen eines Dienstprinzipals nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="65846-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="65846-115">Entfernt den Dienstprinzipal mit der Objekt-ID '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span><span class="sxs-lookup"><span data-stu-id="65846-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="65846-116">Beispiel 2: Entfernen eines Dienstprinzipals nach Anwendungs-ID</span><span class="sxs-lookup"><span data-stu-id="65846-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="65846-117">Entfernt den Dienstprinzipal mit der Anwendungs-ID '9263469e-d328-4321-8646-3e3e75d20e76'.</span><span class="sxs-lookup"><span data-stu-id="65846-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="65846-118">Beispiel 3: Entfernen eines Dienstprinzipals durch SPN</span><span class="sxs-lookup"><span data-stu-id="65846-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="65846-119">Entfernen des Dienstprinzipals mit dem Dienstprinzipalnamen "MyServicePrincipal"</span><span class="sxs-lookup"><span data-stu-id="65846-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="65846-120">Beispiel 4: Entfernen eines Dienstprinzipal durch Piping</span><span class="sxs-lookup"><span data-stu-id="65846-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

<span data-ttu-id="65846-121">Ruft den Dienstprinzipal mit der Objekt-ID '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' ab und gibt diese an das Cmdlet Remove-AzADServicePrincipal weiter, um diesen Dienstprinzipal zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="65846-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="65846-122">Beispiel 5: Entfernen eines Dienstprinzipal durch Hinzufügen einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="65846-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

<span data-ttu-id="65846-123">Ruft die Anwendung mit der Anwendungs-ID '9263469e-d328-4321-8646-3e3e75d20e76' ab und gibt diese an das cmdlet Remove-AzADServicePrincipal weiter, um den dienstprinzipal zu entfernen, der dieser Anwendung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="65846-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="65846-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65846-124">PARAMETERS</span></span>

### <span data-ttu-id="65846-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="65846-125">-ApplicationId</span></span>
<span data-ttu-id="65846-126">Die Dienstprinzipalanwendungs-ID.</span><span class="sxs-lookup"><span data-stu-id="65846-126">The service principal application id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65846-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="65846-127">-ApplicationObject</span></span>
<span data-ttu-id="65846-128">Das Anwendungsobjekt, dessen Dienstprinzipal entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="65846-128">The application object whose service principal is being removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65846-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65846-129">-DefaultProfile</span></span>
<span data-ttu-id="65846-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="65846-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65846-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="65846-131">-DisplayName</span></span>
<span data-ttu-id="65846-132">Der Anzeigename des Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="65846-132">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65846-133">-Force</span><span class="sxs-lookup"><span data-stu-id="65846-133">-Force</span></span>
<span data-ttu-id="65846-134">Wechseln sie zum Löschen des Dienstprinzipals ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="65846-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="65846-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65846-135">-InputObject</span></span>
<span data-ttu-id="65846-136">Das Dienstprinzipalobjekt.</span><span class="sxs-lookup"><span data-stu-id="65846-136">The service principal object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65846-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="65846-137">-ObjectId</span></span>
<span data-ttu-id="65846-138">Die Objekt-ID des zu löschende Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="65846-138">The object id of the service principal to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65846-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65846-139">-PassThru</span></span>
<span data-ttu-id="65846-140">Wenn angegeben, wird der gelöschte Dienstprinzipal zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="65846-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="65846-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="65846-141">-ServicePrincipalName</span></span>
<span data-ttu-id="65846-142">Der Dienstprinzipalname.</span><span class="sxs-lookup"><span data-stu-id="65846-142">The service principal name.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65846-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65846-143">-Confirm</span></span>
<span data-ttu-id="65846-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="65846-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65846-145">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="65846-145">-WhatIf</span></span>
<span data-ttu-id="65846-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65846-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65846-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="65846-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65846-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65846-148">CommonParameters</span></span>
<span data-ttu-id="65846-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65846-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65846-150">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65846-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65846-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="65846-151">INPUTS</span></span>

### <span data-ttu-id="65846-152">System.String</span><span class="sxs-lookup"><span data-stu-id="65846-152">System.String</span></span>

### <span data-ttu-id="65846-153">System.Guid</span><span class="sxs-lookup"><span data-stu-id="65846-153">System.Guid</span></span>

### <span data-ttu-id="65846-154">Microsoft.Azure.Commands.ActiveDirectory.WAHLDServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="65846-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="65846-155">Microsoft.Azure.Commands.ActiveDirectory.WERDENDApplication</span><span class="sxs-lookup"><span data-stu-id="65846-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="65846-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="65846-156">OUTPUTS</span></span>

### <span data-ttu-id="65846-157">Microsoft.Azure.Commands.ActiveDirectory.WAHLDServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="65846-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="65846-158">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="65846-158">NOTES</span></span>
<span data-ttu-id="65846-159">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="65846-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="65846-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="65846-160">RELATED LINKS</span></span>

[<span data-ttu-id="65846-161">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="65846-161">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="65846-162">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="65846-162">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="65846-163">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="65846-163">Update-AzADServicePrincipal</span></span>](./Update-AzADServicePrincipal.md)

[<span data-ttu-id="65846-164">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="65846-164">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="65846-165">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="65846-165">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)
