---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: 8799450cc73784b45804ea1fa26785716a895bed
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399582"
---
# <span data-ttu-id="86599-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="86599-101">Remove-AzADUser</span></span>

## <span data-ttu-id="86599-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86599-102">SYNOPSIS</span></span>
<span data-ttu-id="86599-103">Löscht einen Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="86599-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="86599-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86599-104">SYNTAX</span></span>

### <span data-ttu-id="86599-105">UPNOrObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="86599-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86599-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="86599-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86599-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86599-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86599-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="86599-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86599-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86599-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86599-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86599-110">DESCRIPTION</span></span>
<span data-ttu-id="86599-111">Löscht einen Active Directory-Benutzer (Arbeits-/Schulkonto, auch als Organisations-ID bekannt).</span><span class="sxs-lookup"><span data-stu-id="86599-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="86599-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="86599-112">EXAMPLES</span></span>

### <span data-ttu-id="86599-113">Beispiel 1: Entfernen eines Benutzers nach Benutzerprinzipalnamen</span><span class="sxs-lookup"><span data-stu-id="86599-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="86599-114">Entfernt den Benutzer mit dem Benutzerprinzipalnamen " foo@domain.com " aus dem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="86599-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="86599-115">Beispiel 2: Entfernen eines Benutzers nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="86599-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="86599-116">Entfernt den Benutzer mit der Objekt-ID '7a9582cf-88c4-4319-842b-7a5d60967a69' aus dem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="86599-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="86599-117">Beispiel 3: Entfernen eines Benutzers durch Piping</span><span class="sxs-lookup"><span data-stu-id="86599-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="86599-118">Ruft den Benutzer mit der Objekt-ID '7a9582cf-88c4-4319-842b-7a5d60967a69' ab und gibt diese an das Cmdlet Remove-AzADUser weiter, um den Benutzer aus dem Mandanten zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="86599-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="86599-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86599-119">PARAMETERS</span></span>

### <span data-ttu-id="86599-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86599-120">-DefaultProfile</span></span>
<span data-ttu-id="86599-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="86599-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86599-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="86599-122">-DisplayName</span></span>
<span data-ttu-id="86599-123">Der Anzeigename des zu löschende Benutzers.</span><span class="sxs-lookup"><span data-stu-id="86599-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="86599-124">-Force</span><span class="sxs-lookup"><span data-stu-id="86599-124">-Force</span></span>
<span data-ttu-id="86599-125">Falls angegeben, wird nicht zur Bestätigung des Löschens des Benutzers gefragt.</span><span class="sxs-lookup"><span data-stu-id="86599-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="86599-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86599-126">-InputObject</span></span>
<span data-ttu-id="86599-127">Das zu löschende Benutzerobjekt.</span><span class="sxs-lookup"><span data-stu-id="86599-127">The user object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADUser
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86599-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="86599-128">-ObjectId</span></span>
<span data-ttu-id="86599-129">Die Objekt-ID des zu löschende Benutzers.</span><span class="sxs-lookup"><span data-stu-id="86599-129">The object id of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86599-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86599-130">-PassThru</span></span>
<span data-ttu-id="86599-131">Wenn Sie diese Angabe angeben, wird "true" zurückgeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="86599-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="86599-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="86599-132">-UPNOrObjectId</span></span>
<span data-ttu-id="86599-133">Der Benutzerprinzipalname oder die objectId des zu löschenden Benutzers.</span><span class="sxs-lookup"><span data-stu-id="86599-133">The user principal name or the objectId of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86599-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="86599-134">-UserPrincipalName</span></span>
<span data-ttu-id="86599-135">Der Benutzerprinzipalname des zu löschende Benutzers.</span><span class="sxs-lookup"><span data-stu-id="86599-135">The user principal name of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86599-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86599-136">-Confirm</span></span>
<span data-ttu-id="86599-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="86599-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86599-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="86599-138">-WhatIf</span></span>
<span data-ttu-id="86599-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="86599-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86599-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="86599-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86599-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86599-141">CommonParameters</span></span>
<span data-ttu-id="86599-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86599-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86599-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86599-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86599-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="86599-144">INPUTS</span></span>

### <span data-ttu-id="86599-145">System.String</span><span class="sxs-lookup"><span data-stu-id="86599-145">System.String</span></span>

### <span data-ttu-id="86599-146">Microsoft.Azure.Commands.ActiveDirectory.WERDENDUser</span><span class="sxs-lookup"><span data-stu-id="86599-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="86599-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="86599-147">OUTPUTS</span></span>

### <span data-ttu-id="86599-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="86599-148">System.Boolean</span></span>

## <span data-ttu-id="86599-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="86599-149">NOTES</span></span>

## <span data-ttu-id="86599-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="86599-150">RELATED LINKS</span></span>

[<span data-ttu-id="86599-151">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="86599-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="86599-152">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="86599-152">Get-AzADUser</span></span>](./Get-AzADUser.md)


