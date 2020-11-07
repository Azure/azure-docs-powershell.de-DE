---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: 2dc9a0d3d41ca1bccb131e92cf514fd2f814943b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659559"
---
# <span data-ttu-id="a0fe8-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="a0fe8-101">Remove-AzADUser</span></span>

## <span data-ttu-id="a0fe8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0fe8-102">SYNOPSIS</span></span>
<span data-ttu-id="a0fe8-103">Löscht einen Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="a0fe8-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="a0fe8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0fe8-104">SYNTAX</span></span>

### <span data-ttu-id="a0fe8-105">UPNOrObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0fe8-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0fe8-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0fe8-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0fe8-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0fe8-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0fe8-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0fe8-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0fe8-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0fe8-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0fe8-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0fe8-110">DESCRIPTION</span></span>
<span data-ttu-id="a0fe8-111">Löscht einen Active Directory-Benutzer (Firmen-oder Schulkonto, auch bekannt als org-ID).</span><span class="sxs-lookup"><span data-stu-id="a0fe8-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="a0fe8-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0fe8-112">EXAMPLES</span></span>

### <span data-ttu-id="a0fe8-113">Beispiel 1: Entfernen eines Benutzers nach dem Benutzerprinzipalnamen</span><span class="sxs-lookup"><span data-stu-id="a0fe8-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="a0fe8-114">Entfernt den Benutzer mit dem Benutzerprinzipalnamen " foo@domain.com " aus dem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="a0fe8-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="a0fe8-115">Beispiel 2 – Entfernen eines Benutzers nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="a0fe8-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="a0fe8-116">Entfernt den Benutzer mit der Objekt-ID "7a9582cf-88c4-4319-842b-7a5d60967a69" aus dem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="a0fe8-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="a0fe8-117">Beispiel 3: Entfernen eines Benutzers durch Verrohrung</span><span class="sxs-lookup"><span data-stu-id="a0fe8-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="a0fe8-118">Ruft den Benutzer mit der Objekt-ID "7a9582cf-88c4-4319-842b-7a5d60967a69" und Pipes an das Remove-AzADUser-Cmdlet ab, um den Benutzer aus dem Mandanten zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="a0fe8-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="a0fe8-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0fe8-119">PARAMETERS</span></span>

### <span data-ttu-id="a0fe8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0fe8-120">-DefaultProfile</span></span>
<span data-ttu-id="a0fe8-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a0fe8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0fe8-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a0fe8-122">-DisplayName</span></span>
<span data-ttu-id="a0fe8-123">Der Anzeigename des Benutzers, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0fe8-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="a0fe8-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a0fe8-124">-Force</span></span>
<span data-ttu-id="a0fe8-125">Wenn angegeben, wird keine Bestätigung zum Löschen des Benutzers verlangt.</span><span class="sxs-lookup"><span data-stu-id="a0fe8-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="a0fe8-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a0fe8-126">-InputObject</span></span>
<span data-ttu-id="a0fe8-127">Das Benutzerobjekt, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0fe8-127">The user object to be deleted.</span></span>

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

### <span data-ttu-id="a0fe8-128">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="a0fe8-128">-ObjectId</span></span>
<span data-ttu-id="a0fe8-129">Die Objekt-ID des Benutzers, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0fe8-129">The object id of the user to be deleted.</span></span>

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

### <span data-ttu-id="a0fe8-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0fe8-130">-PassThru</span></span>
<span data-ttu-id="a0fe8-131">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="a0fe8-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="a0fe8-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="a0fe8-132">-UPNOrObjectId</span></span>
<span data-ttu-id="a0fe8-133">Der Benutzerprinzipalname oder die ObjectID des Benutzers, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0fe8-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="a0fe8-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a0fe8-134">-UserPrincipalName</span></span>
<span data-ttu-id="a0fe8-135">Der Benutzerprinzipalname des Benutzers, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0fe8-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="a0fe8-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a0fe8-136">-Confirm</span></span>
<span data-ttu-id="a0fe8-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0fe8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0fe8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0fe8-138">-WhatIf</span></span>
<span data-ttu-id="a0fe8-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0fe8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0fe8-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0fe8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0fe8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0fe8-141">CommonParameters</span></span>
<span data-ttu-id="a0fe8-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0fe8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0fe8-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0fe8-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0fe8-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0fe8-144">INPUTS</span></span>

### <span data-ttu-id="a0fe8-145">System. String</span><span class="sxs-lookup"><span data-stu-id="a0fe8-145">System.String</span></span>

### <span data-ttu-id="a0fe8-146">Microsoft. Azure. Commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="a0fe8-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="a0fe8-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0fe8-147">OUTPUTS</span></span>

### <span data-ttu-id="a0fe8-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0fe8-148">System.Boolean</span></span>

## <span data-ttu-id="a0fe8-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0fe8-149">NOTES</span></span>

## <span data-ttu-id="a0fe8-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0fe8-150">RELATED LINKS</span></span>

[<span data-ttu-id="a0fe8-151">Neu – AzADUser</span><span class="sxs-lookup"><span data-stu-id="a0fe8-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="a0fe8-152">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="a0fe8-152">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="a0fe8-153">Satz-AzADUser</span><span class="sxs-lookup"><span data-stu-id="a0fe8-153">Set-AzADUser</span></span>](./Set-AzADUser.md)

