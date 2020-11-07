---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermaduser
schema: 2.0.0
ms.openlocfilehash: 504ce8bd2c7ae5dce3fe859d678b27ad829b2932
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849015"
---
# <span data-ttu-id="0b67c-101">Update-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="0b67c-101">Update-AzureRmADUser</span></span>

## <span data-ttu-id="0b67c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b67c-102">SYNOPSIS</span></span>
<span data-ttu-id="0b67c-103">Aktualisiert einen vorhandenen Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="0b67c-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b67c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b67c-104">SYNTAX</span></span>

### <span data-ttu-id="0b67c-105">UPNOrObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0b67c-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b67c-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b67c-106">UPNParameterSet</span></span>
```
Update-AzureRmADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b67c-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b67c-107">ObjectIdParameterSet</span></span>
```
Update-AzureRmADUser -ObjectId <Guid> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b67c-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b67c-108">InputObjectParameterSet</span></span>
```
Update-AzureRmADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b67c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b67c-109">DESCRIPTION</span></span>
<span data-ttu-id="0b67c-110">Aktualisiert einen vorhandenen Active Directory-Benutzer (Firmen-oder Schulkonto, auch bekannt als org-ID).</span><span class="sxs-lookup"><span data-stu-id="0b67c-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="0b67c-111">Weitere Informationen: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="0b67c-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="0b67c-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b67c-112">EXAMPLES</span></span>

### <span data-ttu-id="0b67c-113">Beispiel 1 – Aktualisieren des Anzeigenamens eines Benutzers mit der Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="0b67c-113">Example 1 - Update the display name of a user using object id</span></span>

```
PS C:\> Update-AzureRmADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="0b67c-114">Aktualisiert den Anzeigenamen des Benutzers mit der Objekt-ID "155a5c10-93a9-4941-a0df-96d83ab5ab24" als "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="0b67c-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="0b67c-115">Beispiel 2 – Aktualisieren des Anzeigenamens eines Benutzers mit dem Benutzerprinzipalnamen</span><span class="sxs-lookup"><span data-stu-id="0b67c-115">Example 2 - Update the display name of a user using user principal name</span></span>

```
PS C:\> Update-AzureRmADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="0b67c-116">Aktualisiert den Anzeigenamen des Benutzers mit dem Benutzerprinzipalnamen " foo@domain.com " als "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="0b67c-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="0b67c-117">Beispiel 3: Aktualisieren des Anzeigenamens eines Benutzers mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="0b67c-117">Example 3 - Update the display name of a user using piping</span></span>

```
PS C:\> Get-AzureRmADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzureRmADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="0b67c-118">Ruft den Benutzer mit der Objekt-ID "155a5c10-93a9-4941-a0df-96d83ab5ab24" und Pipes an das Update-AzureRmADUser-Cmdlet ab, um den Anzeigenamen dieses Benutzers auf "MyNewDisplayName" zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0b67c-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzureRmADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="0b67c-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b67c-119">PARAMETERS</span></span>

### <span data-ttu-id="0b67c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b67c-120">-DefaultProfile</span></span>
<span data-ttu-id="0b67c-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b67c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b67c-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0b67c-122">-DisplayName</span></span>
<span data-ttu-id="0b67c-123">Neuer Anzeigename für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="0b67c-123">New display name for the user.</span></span>

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

### <span data-ttu-id="0b67c-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="0b67c-124">-EnableAccount</span></span>
<span data-ttu-id="0b67c-125">true zum Aktivieren des Kontos; andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="0b67c-125">true for enabling the account; otherwise, false.</span></span>

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

### <span data-ttu-id="0b67c-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="0b67c-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="0b67c-127">Sie muss angegeben werden, wenn der Benutzer das Kennwort bei der nächsten erfolgreichen Anmeldung ändern soll.</span><span class="sxs-lookup"><span data-stu-id="0b67c-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="0b67c-128">Nur gültig, wenn das Kennwort aktualisiert wird, andernfalls wird es ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0b67c-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="0b67c-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0b67c-129">-InputObject</span></span>
<span data-ttu-id="0b67c-130">Das Objekt, das den Benutzer darstellt, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b67c-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="0b67c-131">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="0b67c-131">-ObjectId</span></span>
<span data-ttu-id="0b67c-132">Die Objekt-ID des Benutzers, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b67c-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="0b67c-133">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="0b67c-133">-Password</span></span>
<span data-ttu-id="0b67c-134">Neues Kennwort für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="0b67c-134">New password for the user.</span></span>

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

### <span data-ttu-id="0b67c-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="0b67c-135">-UPNOrObjectId</span></span>
<span data-ttu-id="0b67c-136">Der Benutzerprinzipalname oder die Objekt-ID des Benutzers, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b67c-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="0b67c-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="0b67c-137">-UserPrincipalName</span></span>
<span data-ttu-id="0b67c-138">Der Benutzerprinzipalname des Benutzers, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b67c-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="0b67c-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b67c-139">-Confirm</span></span>
<span data-ttu-id="0b67c-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b67c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b67c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b67c-141">-WhatIf</span></span>
<span data-ttu-id="0b67c-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b67c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b67c-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b67c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b67c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b67c-144">CommonParameters</span></span>
<span data-ttu-id="0b67c-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b67c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b67c-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b67c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b67c-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b67c-147">INPUTS</span></span>

### <span data-ttu-id="0b67c-148">System. String</span><span class="sxs-lookup"><span data-stu-id="0b67c-148">System.String</span></span>

### <span data-ttu-id="0b67c-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="0b67c-149">System.Guid</span></span>

### <span data-ttu-id="0b67c-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="0b67c-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="0b67c-151">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0b67c-151">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0b67c-152">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0b67c-152">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="0b67c-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="0b67c-153">System.Security.SecureString</span></span>

## <span data-ttu-id="0b67c-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b67c-154">OUTPUTS</span></span>

### <span data-ttu-id="0b67c-155">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="0b67c-155">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="0b67c-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b67c-156">NOTES</span></span>

## <span data-ttu-id="0b67c-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b67c-157">RELATED LINKS</span></span>
