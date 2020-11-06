---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmADUser.md
ms.openlocfilehash: a07d9119d5e83c92d96ab22e98125459945f786b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482085"
---
# <span data-ttu-id="889e2-101">Update-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="889e2-101">Update-AzureRmADUser</span></span>

## <span data-ttu-id="889e2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="889e2-102">SYNOPSIS</span></span>
<span data-ttu-id="889e2-103">Aktualisiert einen vorhandenen Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="889e2-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="889e2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="889e2-104">SYNTAX</span></span>

### <span data-ttu-id="889e2-105">UPNOrObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="889e2-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="889e2-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="889e2-106">UPNParameterSet</span></span>
```
Update-AzureRmADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="889e2-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="889e2-107">ObjectIdParameterSet</span></span>
```
Update-AzureRmADUser -ObjectId <Guid> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="889e2-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="889e2-108">InputObjectParameterSet</span></span>
```
Update-AzureRmADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="889e2-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="889e2-109">DESCRIPTION</span></span>
<span data-ttu-id="889e2-110">Aktualisiert einen vorhandenen Active Directory-Benutzer (Firmen-oder Schulkonto, auch bekannt als org-ID).</span><span class="sxs-lookup"><span data-stu-id="889e2-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="889e2-111">Weitere Informationen: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="889e2-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="889e2-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="889e2-112">EXAMPLES</span></span>

### <span data-ttu-id="889e2-113">Beispiel 1 – Aktualisieren des Anzeigenamens eines Benutzers mit der Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="889e2-113">Example 1 - Update the display name of a user using object id</span></span>

```
PS C:\> Update-AzureRmADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="889e2-114">Aktualisiert den Anzeigenamen des Benutzers mit der Objekt-ID "155a5c10-93a9-4941-a0df-96d83ab5ab24" als "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="889e2-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="889e2-115">Beispiel 2 – Aktualisieren des Anzeigenamens eines Benutzers mit dem Benutzerprinzipalnamen</span><span class="sxs-lookup"><span data-stu-id="889e2-115">Example 2 - Update the display name of a user using user principal name</span></span>

```
PS C:\> Update-AzureRmADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="889e2-116">Aktualisiert den Anzeigenamen des Benutzers mit dem Benutzerprinzipalnamen " foo@domain.com " als "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="889e2-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="889e2-117">Beispiel 3: Aktualisieren des Anzeigenamens eines Benutzers mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="889e2-117">Example 3 - Update the display name of a user using piping</span></span>

```
PS C:\> Get-AzureRmADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzureRmADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="889e2-118">Ruft den Benutzer mit der Objekt-ID "155a5c10-93a9-4941-a0df-96d83ab5ab24" und Pipes an das Update-AzureRmADUser-Cmdlet ab, um den Anzeigenamen dieses Benutzers auf "MyNewDisplayName" zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="889e2-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzureRmADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="889e2-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="889e2-119">PARAMETERS</span></span>

### <span data-ttu-id="889e2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="889e2-120">-DefaultProfile</span></span>
<span data-ttu-id="889e2-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="889e2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="889e2-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="889e2-122">-DisplayName</span></span>
<span data-ttu-id="889e2-123">Neuer Anzeigename für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="889e2-123">New display name for the user.</span></span>

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

### <span data-ttu-id="889e2-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="889e2-124">-EnableAccount</span></span>
<span data-ttu-id="889e2-125">true zum Aktivieren des Kontos; andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="889e2-125">true for enabling the account; otherwise, false.</span></span>

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

### <span data-ttu-id="889e2-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="889e2-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="889e2-127">Sie muss angegeben werden, wenn der Benutzer das Kennwort bei der nächsten erfolgreichen Anmeldung ändern soll.</span><span class="sxs-lookup"><span data-stu-id="889e2-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="889e2-128">Nur gültig, wenn das Kennwort aktualisiert wird, andernfalls wird es ignoriert.</span><span class="sxs-lookup"><span data-stu-id="889e2-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="889e2-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="889e2-129">-InputObject</span></span>
<span data-ttu-id="889e2-130">Das Objekt, das den Benutzer darstellt, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="889e2-130">The object representing the user to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="889e2-131">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="889e2-131">-ObjectId</span></span>
<span data-ttu-id="889e2-132">Die Objekt-ID des Benutzers, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="889e2-132">The object id of the user to be updated.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="889e2-133">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="889e2-133">-Password</span></span>
<span data-ttu-id="889e2-134">Neues Kennwort für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="889e2-134">New password for the user.</span></span>

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

### <span data-ttu-id="889e2-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="889e2-135">-UPNOrObjectId</span></span>
<span data-ttu-id="889e2-136">Der Benutzerprinzipalname oder die Objekt-ID des Benutzers, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="889e2-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="889e2-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="889e2-137">-UserPrincipalName</span></span>
<span data-ttu-id="889e2-138">Der Benutzerprinzipalname des Benutzers, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="889e2-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="889e2-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="889e2-139">-Confirm</span></span>
<span data-ttu-id="889e2-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="889e2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="889e2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="889e2-141">-WhatIf</span></span>
<span data-ttu-id="889e2-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="889e2-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="889e2-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="889e2-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="889e2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="889e2-144">CommonParameters</span></span>
<span data-ttu-id="889e2-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="889e2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="889e2-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="889e2-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="889e2-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="889e2-147">INPUTS</span></span>

### <span data-ttu-id="889e2-148">System. String</span><span class="sxs-lookup"><span data-stu-id="889e2-148">System.String</span></span>

### <span data-ttu-id="889e2-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="889e2-149">System.Guid</span></span>

### <span data-ttu-id="889e2-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="889e2-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="889e2-151">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="889e2-151">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="889e2-152">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="889e2-152">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="889e2-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="889e2-153">System.Security.SecureString</span></span>

## <span data-ttu-id="889e2-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="889e2-154">OUTPUTS</span></span>

### <span data-ttu-id="889e2-155">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="889e2-155">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="889e2-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="889e2-156">NOTES</span></span>

## <span data-ttu-id="889e2-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="889e2-157">RELATED LINKS</span></span>
