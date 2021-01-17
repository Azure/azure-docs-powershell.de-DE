---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
ms.openlocfilehash: b765e33479c6178d69fb670a2f18ef0169eadf35
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290800"
---
# <span data-ttu-id="55872-101">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="55872-101">Update-AzADUser</span></span>

## <span data-ttu-id="55872-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55872-102">SYNOPSIS</span></span>
<span data-ttu-id="55872-103">Aktualisiert einen vorhandenen Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="55872-103">Updates an existing active directory user.</span></span>

## <span data-ttu-id="55872-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55872-104">SYNTAX</span></span>

### <span data-ttu-id="55872-105">UPNOrObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="55872-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55872-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="55872-106">UPNParameterSet</span></span>
```
Update-AzADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55872-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55872-107">ObjectIdParameterSet</span></span>
```
Update-AzADUser -ObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55872-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55872-108">InputObjectParameterSet</span></span>
```
Update-AzADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55872-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55872-109">DESCRIPTION</span></span>
<span data-ttu-id="55872-110">Aktualisiert einen vorhandenen Active Directory-Benutzer (Arbeits-/Schulkonto, auch als Organisations-ID bekannt).</span><span class="sxs-lookup"><span data-stu-id="55872-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="55872-111">Weitere Informationen: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="55872-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="55872-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="55872-112">EXAMPLES</span></span>

### <span data-ttu-id="55872-113">Beispiel 1: Aktualisieren des Anzeigenamens eines Benutzers mithilfe der Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="55872-113">Example 1: Update the display name of a user using object id</span></span>

```powershell
PS C:\> Update-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="55872-114">Aktualisiert den Anzeigenamen des Benutzers mit der Objekt-ID '155a5c10-93a9-4941-a0df-96d83ab5ab24' in 'MyNewDisplayName'.</span><span class="sxs-lookup"><span data-stu-id="55872-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="55872-115">Beispiel 2: Aktualisieren des Anzeigenamens eines Benutzers unter Verwendung des Benutzerprinzipalnamens</span><span class="sxs-lookup"><span data-stu-id="55872-115">Example 2: Update the display name of a user using user principal name</span></span>

```powershell
PS C:\> Update-AzADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="55872-116">Aktualisiert den Anzeigenamen des Benutzers mit dem Benutzerprinzipalnamen foo@domain.com ' in 'MyNewDisplayName'.</span><span class="sxs-lookup"><span data-stu-id="55872-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="55872-117">Beispiel 3: Aktualisieren des Anzeigenamens eines Benutzers mithilfe der Piping</span><span class="sxs-lookup"><span data-stu-id="55872-117">Example 3: Update the display name of a user using piping</span></span>

```powershell
PS C:\> Get-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="55872-118">Ruft den Benutzer mit der Objekt-ID '155a5c10-93a9-4941-a0df-96d83ab5ab24' ab und gibt diese an das cmdlet Update-AzADUser weiter, um den Anzeigenamen dieses Benutzers auf "MyNewDisplayName" zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="55872-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="55872-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55872-119">PARAMETERS</span></span>

### <span data-ttu-id="55872-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55872-120">-DefaultProfile</span></span>
<span data-ttu-id="55872-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55872-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55872-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="55872-122">-DisplayName</span></span>
<span data-ttu-id="55872-123">Neuer Anzeigename für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="55872-123">New display name for the user.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55872-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="55872-124">-EnableAccount</span></span>
<span data-ttu-id="55872-125">true für die Aktivierung des Kontos; andernfalls "false".</span><span class="sxs-lookup"><span data-stu-id="55872-125">true for enabling the account; otherwise, false.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55872-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="55872-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="55872-127">Es muss angegeben werden, wenn der Benutzer das Kennwort bei der nächsten erfolgreichen Anmeldung ändern soll.</span><span class="sxs-lookup"><span data-stu-id="55872-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="55872-128">Nur gültig, wenn das Kennwort aktualisiert wird, andernfalls wird es ignoriert.</span><span class="sxs-lookup"><span data-stu-id="55872-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="55872-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55872-129">-InputObject</span></span>
<span data-ttu-id="55872-130">Das Objekt, das den zu aktualisierenden Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="55872-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="55872-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="55872-131">-ObjectId</span></span>
<span data-ttu-id="55872-132">Die Objekt-ID des Benutzers, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="55872-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="55872-133">-Password</span><span class="sxs-lookup"><span data-stu-id="55872-133">-Password</span></span>
<span data-ttu-id="55872-134">Neues Kennwort für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="55872-134">New password for the user.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55872-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="55872-135">-UPNOrObjectId</span></span>
<span data-ttu-id="55872-136">Der Benutzerprinzipalname oder die Objekt-ID des Benutzers, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="55872-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="55872-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="55872-137">-UserPrincipalName</span></span>
<span data-ttu-id="55872-138">Der Benutzerprinzipalname des Benutzers, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="55872-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="55872-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55872-139">-Confirm</span></span>
<span data-ttu-id="55872-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55872-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55872-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="55872-141">-WhatIf</span></span>
<span data-ttu-id="55872-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55872-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55872-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55872-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55872-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55872-144">CommonParameters</span></span>
<span data-ttu-id="55872-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55872-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55872-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55872-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55872-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="55872-147">INPUTS</span></span>

### <span data-ttu-id="55872-148">System.String</span><span class="sxs-lookup"><span data-stu-id="55872-148">System.String</span></span>

### <span data-ttu-id="55872-149">Microsoft.Azure.Commands.ActiveDirectory.WERDENDUser</span><span class="sxs-lookup"><span data-stu-id="55872-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

### <span data-ttu-id="55872-150">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="55872-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="55872-151">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="55872-151">System.Security.SecureString</span></span>

## <span data-ttu-id="55872-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="55872-152">OUTPUTS</span></span>

### <span data-ttu-id="55872-153">Microsoft.Azure.Commands.ActiveDirectory.WERDENDUser</span><span class="sxs-lookup"><span data-stu-id="55872-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="55872-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="55872-154">NOTES</span></span>

## <span data-ttu-id="55872-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="55872-155">RELATED LINKS</span></span>
