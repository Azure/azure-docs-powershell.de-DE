---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
ms.openlocfilehash: 991b81e9314c5f9c1959e8f352f8c2e218a1b701
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845828"
---
# <span data-ttu-id="afe4b-101">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="afe4b-101">Update-AzADUser</span></span>

## <span data-ttu-id="afe4b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="afe4b-102">SYNOPSIS</span></span>
<span data-ttu-id="afe4b-103">Aktualisiert einen vorhandenen Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="afe4b-103">Updates an existing active directory user.</span></span>

## <span data-ttu-id="afe4b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="afe4b-104">SYNTAX</span></span>

### <span data-ttu-id="afe4b-105">UPNOrObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="afe4b-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afe4b-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="afe4b-106">UPNParameterSet</span></span>
```
Update-AzADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afe4b-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="afe4b-107">ObjectIdParameterSet</span></span>
```
Update-AzADUser -ObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afe4b-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="afe4b-108">InputObjectParameterSet</span></span>
```
Update-AzADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afe4b-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="afe4b-109">DESCRIPTION</span></span>
<span data-ttu-id="afe4b-110">Aktualisiert einen vorhandenen Active Directory-Benutzer (Firmen-oder Schulkonto, auch bekannt als org-ID).</span><span class="sxs-lookup"><span data-stu-id="afe4b-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="afe4b-111">Weitere Informationen: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="afe4b-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="afe4b-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="afe4b-112">EXAMPLES</span></span>

### <span data-ttu-id="afe4b-113">Beispiel 1 – Aktualisieren des Anzeigenamens eines Benutzers mit der Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="afe4b-113">Example 1 - Update the display name of a user using object id</span></span>

```
PS C:\> Update-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="afe4b-114">Aktualisiert den Anzeigenamen des Benutzers mit der Objekt-ID "155a5c10-93a9-4941-a0df-96d83ab5ab24" als "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="afe4b-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="afe4b-115">Beispiel 2 – Aktualisieren des Anzeigenamens eines Benutzers mit dem Benutzerprinzipalnamen</span><span class="sxs-lookup"><span data-stu-id="afe4b-115">Example 2 - Update the display name of a user using user principal name</span></span>

```
PS C:\> Update-AzADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="afe4b-116">Aktualisiert den Anzeigenamen des Benutzers mit dem Benutzerprinzipalnamen " foo@domain.com " als "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="afe4b-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="afe4b-117">Beispiel 3: Aktualisieren des Anzeigenamens eines Benutzers mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="afe4b-117">Example 3 - Update the display name of a user using piping</span></span>

```
PS C:\> Get-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="afe4b-118">Ruft den Benutzer mit der Objekt-ID "155a5c10-93a9-4941-a0df-96d83ab5ab24" und Pipes an das Update-AzADUser-Cmdlet ab, um den Anzeigenamen dieses Benutzers auf "MyNewDisplayName" zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="afe4b-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="afe4b-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="afe4b-119">PARAMETERS</span></span>

### <span data-ttu-id="afe4b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afe4b-120">-DefaultProfile</span></span>
<span data-ttu-id="afe4b-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="afe4b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afe4b-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="afe4b-122">-DisplayName</span></span>
<span data-ttu-id="afe4b-123">Neuer Anzeigename für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="afe4b-123">New display name for the user.</span></span>

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

### <span data-ttu-id="afe4b-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="afe4b-124">-EnableAccount</span></span>
<span data-ttu-id="afe4b-125">true zum Aktivieren des Kontos; andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="afe4b-125">true for enabling the account; otherwise, false.</span></span>

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

### <span data-ttu-id="afe4b-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="afe4b-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="afe4b-127">Sie muss angegeben werden, wenn der Benutzer das Kennwort bei der nächsten erfolgreichen Anmeldung ändern soll.</span><span class="sxs-lookup"><span data-stu-id="afe4b-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="afe4b-128">Nur gültig, wenn das Kennwort aktualisiert wird, andernfalls wird es ignoriert.</span><span class="sxs-lookup"><span data-stu-id="afe4b-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="afe4b-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="afe4b-129">-InputObject</span></span>
<span data-ttu-id="afe4b-130">Das Objekt, das den Benutzer darstellt, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="afe4b-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="afe4b-131">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="afe4b-131">-ObjectId</span></span>
<span data-ttu-id="afe4b-132">Die Objekt-ID des Benutzers, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="afe4b-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="afe4b-133">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="afe4b-133">-Password</span></span>
<span data-ttu-id="afe4b-134">Neues Kennwort für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="afe4b-134">New password for the user.</span></span>

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

### <span data-ttu-id="afe4b-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="afe4b-135">-UPNOrObjectId</span></span>
<span data-ttu-id="afe4b-136">Der Benutzerprinzipalname oder die Objekt-ID des Benutzers, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="afe4b-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="afe4b-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="afe4b-137">-UserPrincipalName</span></span>
<span data-ttu-id="afe4b-138">Der Benutzerprinzipalname des Benutzers, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="afe4b-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="afe4b-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="afe4b-139">-Confirm</span></span>
<span data-ttu-id="afe4b-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="afe4b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afe4b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afe4b-141">-WhatIf</span></span>
<span data-ttu-id="afe4b-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="afe4b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afe4b-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="afe4b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afe4b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afe4b-144">CommonParameters</span></span>
<span data-ttu-id="afe4b-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afe4b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afe4b-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afe4b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afe4b-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="afe4b-147">INPUTS</span></span>

### <span data-ttu-id="afe4b-148">System. String</span><span class="sxs-lookup"><span data-stu-id="afe4b-148">System.String</span></span>

### <span data-ttu-id="afe4b-149">Microsoft. Azure. Commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="afe4b-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

### <span data-ttu-id="afe4b-150">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="afe4b-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="afe4b-151">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="afe4b-151">System.Security.SecureString</span></span>

## <span data-ttu-id="afe4b-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="afe4b-152">OUTPUTS</span></span>

### <span data-ttu-id="afe4b-153">Microsoft. Azure. Commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="afe4b-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="afe4b-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="afe4b-154">NOTES</span></span>

## <span data-ttu-id="afe4b-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="afe4b-155">RELATED LINKS</span></span>
