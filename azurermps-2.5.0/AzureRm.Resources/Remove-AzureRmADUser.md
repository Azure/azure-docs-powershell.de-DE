---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermaduser
schema: 2.0.0
ms.openlocfilehash: 51758c5b51c358a60be310405a89666cc56bac2e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848384"
---
# <span data-ttu-id="f0483-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="f0483-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="f0483-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f0483-102">SYNOPSIS</span></span>
<span data-ttu-id="f0483-103">Löscht einen Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="f0483-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0483-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0483-104">SYNTAX</span></span>

### <span data-ttu-id="f0483-105">UPNOrObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f0483-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0483-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0483-106">UPNParameterSet</span></span>
```
Remove-AzureRmADUser -UserPrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0483-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0483-107">ObjectIdParameterSet</span></span>
```
Remove-AzureRmADUser -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0483-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0483-108">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0483-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0483-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0483-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0483-110">DESCRIPTION</span></span>
<span data-ttu-id="f0483-111">Löscht einen Active Directory-Benutzer (Firmen-oder Schulkonto, auch bekannt als org-ID).</span><span class="sxs-lookup"><span data-stu-id="f0483-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="f0483-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0483-112">EXAMPLES</span></span>

### <span data-ttu-id="f0483-113">Beispiel 1: Entfernen eines Benutzers nach dem Benutzerprinzipalnamen</span><span class="sxs-lookup"><span data-stu-id="f0483-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzureRmADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="f0483-114">Entfernt den Benutzer mit dem Benutzerprinzipalnamen " foo@domain.com " aus dem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="f0483-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="f0483-115">Beispiel 2 – Entfernen eines Benutzers nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="f0483-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzureRmADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="f0483-116">Entfernt den Benutzer mit der Objekt-ID "7a9582cf-88c4-4319-842b-7a5d60967a69" aus dem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="f0483-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="f0483-117">Beispiel 3: Entfernen eines Benutzers durch Verrohrung</span><span class="sxs-lookup"><span data-stu-id="f0483-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzureRmADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzureRmADUser
```

<span data-ttu-id="f0483-118">Ruft den Benutzer mit der Objekt-ID "7a9582cf-88c4-4319-842b-7a5d60967a69" und Pipes an das Remove-AzureRmADUser-Cmdlet ab, um den Benutzer aus dem Mandanten zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="f0483-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzureRmADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="f0483-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0483-119">PARAMETERS</span></span>

### <span data-ttu-id="f0483-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0483-120">-DefaultProfile</span></span>
<span data-ttu-id="f0483-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f0483-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0483-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f0483-122">-DisplayName</span></span>
<span data-ttu-id="f0483-123">Der Anzeigename des Benutzers, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0483-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="f0483-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f0483-124">-Force</span></span>
<span data-ttu-id="f0483-125">Wenn angegeben, wird keine Bestätigung zum Löschen des Benutzers verlangt.</span><span class="sxs-lookup"><span data-stu-id="f0483-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="f0483-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f0483-126">-InputObject</span></span>
<span data-ttu-id="f0483-127">Das Benutzerobjekt, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0483-127">The user object to be deleted.</span></span>

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

### <span data-ttu-id="f0483-128">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="f0483-128">-ObjectId</span></span>
<span data-ttu-id="f0483-129">Die Objekt-ID des Benutzers, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0483-129">The object id of the user to be deleted.</span></span>

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

### <span data-ttu-id="f0483-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0483-130">-PassThru</span></span>
<span data-ttu-id="f0483-131">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="f0483-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f0483-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="f0483-132">-UPNOrObjectId</span></span>
<span data-ttu-id="f0483-133">Der Benutzerprinzipalname oder die ObjectID des Benutzers, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0483-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="f0483-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f0483-134">-UserPrincipalName</span></span>
<span data-ttu-id="f0483-135">Der Benutzerprinzipalname des Benutzers, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0483-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="f0483-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f0483-136">-Confirm</span></span>
<span data-ttu-id="f0483-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0483-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0483-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0483-138">-WhatIf</span></span>
<span data-ttu-id="f0483-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0483-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0483-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0483-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0483-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0483-141">CommonParameters</span></span>
<span data-ttu-id="f0483-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0483-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0483-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0483-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0483-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f0483-144">INPUTS</span></span>

### <span data-ttu-id="f0483-145">System. String</span><span class="sxs-lookup"><span data-stu-id="f0483-145">System.String</span></span>

### <span data-ttu-id="f0483-146">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f0483-146">System.Guid</span></span>

### <span data-ttu-id="f0483-147">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="f0483-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="f0483-148">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f0483-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f0483-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f0483-149">OUTPUTS</span></span>

### <span data-ttu-id="f0483-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f0483-150">System.Boolean</span></span>

## <span data-ttu-id="f0483-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="f0483-151">NOTES</span></span>

## <span data-ttu-id="f0483-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f0483-152">RELATED LINKS</span></span>

[<span data-ttu-id="f0483-153">Neu – AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="f0483-153">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="f0483-154">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="f0483-154">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)



