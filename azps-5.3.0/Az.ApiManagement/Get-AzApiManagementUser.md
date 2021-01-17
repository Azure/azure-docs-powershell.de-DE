---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
ms.openlocfilehash: 44f351870e97d227484bd09be1e75b8cb19ac723
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471447"
---
# <span data-ttu-id="75a9c-101">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="75a9c-101">Get-AzApiManagementUser</span></span>

## <span data-ttu-id="75a9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="75a9c-103">Ruft einen oder mehrere Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="75a9c-103">Gets a user or users.</span></span>

## <span data-ttu-id="75a9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75a9c-104">SYNTAX</span></span>

### <span data-ttu-id="75a9c-105">GeAllUsers (Standard)</span><span class="sxs-lookup"><span data-stu-id="75a9c-105">GeAllUsers (Default)</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75a9c-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="75a9c-106">GetByUserId</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75a9c-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="75a9c-107">GetByUser</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75a9c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75a9c-108">DESCRIPTION</span></span>
<span data-ttu-id="75a9c-109">Das **Cmdlet "Get-AzApiManagementUser"** ruft einen angegebenen Benutzer (oder alle Benutzer) ab, wenn kein Benutzer angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="75a9c-109">The **Get-AzApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="75a9c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="75a9c-110">EXAMPLES</span></span>

### <span data-ttu-id="75a9c-111">Beispiel 1: Alle Benutzer erhalten</span><span class="sxs-lookup"><span data-stu-id="75a9c-111">Example 1: Get all users</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext
```

<span data-ttu-id="75a9c-112">Dieser Befehl ruft alle Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="75a9c-112">This command gets all users.</span></span>

### <span data-ttu-id="75a9c-113">Beispiel 2: Benutzer per ID erhalten</span><span class="sxs-lookup"><span data-stu-id="75a9c-113">Example 2: Get a user by ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="75a9c-114">Dieser Befehl ruft einen Benutzer per ID ab.</span><span class="sxs-lookup"><span data-stu-id="75a9c-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="75a9c-115">Beispiel 3: Benutzer nach Nachname erhalten</span><span class="sxs-lookup"><span data-stu-id="75a9c-115">Example 3: Get users by last name</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="75a9c-116">Dieser Befehl ruft Benutzer mit einem angegebenen Nachnamen namens "Fuller" ab.</span><span class="sxs-lookup"><span data-stu-id="75a9c-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="75a9c-117">Beispiel 4: Erhalten eines Benutzers per E-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="75a9c-117">Example 4: Get a user by email address</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="75a9c-118">Dieser Befehl ruft den Benutzer ab, der über die angegebene E-Mail-Adresse verfügt.</span><span class="sxs-lookup"><span data-stu-id="75a9c-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="75a9c-119">Beispiel 5: Alle Benutzer innerhalb einer Gruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="75a9c-119">Example 5: Get all users within a group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="75a9c-120">Dieser Befehl ruft alle Benutzer innerhalb der angegebenen Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="75a9c-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="75a9c-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75a9c-121">PARAMETERS</span></span>

### <span data-ttu-id="75a9c-122">-Context</span><span class="sxs-lookup"><span data-stu-id="75a9c-122">-Context</span></span>
<span data-ttu-id="75a9c-123">Gibt eine Instanz von **"PsApiManagementContext" an.**</span><span class="sxs-lookup"><span data-stu-id="75a9c-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75a9c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a9c-124">-DefaultProfile</span></span>
<span data-ttu-id="75a9c-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="75a9c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75a9c-126">-E-Mail</span><span class="sxs-lookup"><span data-stu-id="75a9c-126">-Email</span></span>
<span data-ttu-id="75a9c-127">Gibt die E-Mail-Adresse des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="75a9c-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="75a9c-128">Wenn dieser Parameter angegeben ist, findet dieses Cmdlet einen Benutzer per E-Mail.</span><span class="sxs-lookup"><span data-stu-id="75a9c-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="75a9c-129">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="75a9c-129">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a9c-130">-FirstName</span><span class="sxs-lookup"><span data-stu-id="75a9c-130">-FirstName</span></span>
<span data-ttu-id="75a9c-131">Gibt den Vornamen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="75a9c-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="75a9c-132">Wenn dieser Parameter angegeben ist, findet dieses Cmdlet einen Benutzer nach dem Vornamen.</span><span class="sxs-lookup"><span data-stu-id="75a9c-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="75a9c-133">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="75a9c-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a9c-134">-GroupId</span><span class="sxs-lookup"><span data-stu-id="75a9c-134">-GroupId</span></span>
<span data-ttu-id="75a9c-135">Gibt den Gruppenbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="75a9c-135">Specifies the group identifier.</span></span>
<span data-ttu-id="75a9c-136">Falls angegeben, findet dieses Cmdlet alle Benutzer innerhalb der angegebenen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="75a9c-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="75a9c-137">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="75a9c-137">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a9c-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="75a9c-138">-LastName</span></span>
<span data-ttu-id="75a9c-139">Gibt den Nachnamen eines Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="75a9c-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="75a9c-140">Falls angegeben, sucht dieses Cmdlet nach Benutzern nach dem Nachnamen.</span><span class="sxs-lookup"><span data-stu-id="75a9c-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="75a9c-141">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="75a9c-141">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a9c-142">-State</span><span class="sxs-lookup"><span data-stu-id="75a9c-142">-State</span></span>
<span data-ttu-id="75a9c-143">Gibt den Benutzerzustand an.</span><span class="sxs-lookup"><span data-stu-id="75a9c-143">Specifies the user state.</span></span>
<span data-ttu-id="75a9c-144">Falls angegeben, findet dieses Cmdlet Benutzer in diesem Zustand.</span><span class="sxs-lookup"><span data-stu-id="75a9c-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="75a9c-145">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="75a9c-145">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: GetByUser
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a9c-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="75a9c-146">-UserId</span></span>
<span data-ttu-id="75a9c-147">Gibt eine Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="75a9c-147">Specifies a user ID.</span></span>
<span data-ttu-id="75a9c-148">Falls angegeben, findet dieses Cmdlet den Benutzer mit diesem Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="75a9c-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="75a9c-149">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="75a9c-149">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a9c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a9c-150">CommonParameters</span></span>
<span data-ttu-id="75a9c-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75a9c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a9c-152">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75a9c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a9c-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="75a9c-153">INPUTS</span></span>

### <span data-ttu-id="75a9c-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="75a9c-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="75a9c-155">System.String</span><span class="sxs-lookup"><span data-stu-id="75a9c-155">System.String</span></span>

### <span data-ttu-id="75a9c-156">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="75a9c-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="75a9c-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="75a9c-157">OUTPUTS</span></span>

### <span data-ttu-id="75a9c-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="75a9c-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="75a9c-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="75a9c-159">NOTES</span></span>

## <span data-ttu-id="75a9c-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="75a9c-160">RELATED LINKS</span></span>

[<span data-ttu-id="75a9c-161">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="75a9c-161">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="75a9c-162">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="75a9c-162">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)

[<span data-ttu-id="75a9c-163">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="75a9c-163">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


