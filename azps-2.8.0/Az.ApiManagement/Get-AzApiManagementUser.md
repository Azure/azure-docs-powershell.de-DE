---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
ms.openlocfilehash: 6a242334378ceade2f786873181c68f04f8b09a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658290"
---
# <span data-ttu-id="52eb2-101">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="52eb2-101">Get-AzApiManagementUser</span></span>

## <span data-ttu-id="52eb2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="52eb2-102">SYNOPSIS</span></span>
<span data-ttu-id="52eb2-103">Ruft einen Benutzer oder Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="52eb2-103">Gets a user or users.</span></span>

## <span data-ttu-id="52eb2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="52eb2-104">SYNTAX</span></span>

### <span data-ttu-id="52eb2-105">GeAllUsers (Standard)</span><span class="sxs-lookup"><span data-stu-id="52eb2-105">GeAllUsers (Default)</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="52eb2-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="52eb2-106">GetByUserId</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52eb2-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="52eb2-107">GetByUser</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52eb2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52eb2-108">DESCRIPTION</span></span>
<span data-ttu-id="52eb2-109">Das Cmdlet " **Get-AzApiManagementUser** " Ruft einen angegebenen Benutzer oder alle Benutzer ab, wenn kein Benutzer angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="52eb2-109">The **Get-AzApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="52eb2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52eb2-110">EXAMPLES</span></span>

### <span data-ttu-id="52eb2-111">Beispiel 1: Abrufen aller Benutzer</span><span class="sxs-lookup"><span data-stu-id="52eb2-111">Example 1: Get all users</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext
```

<span data-ttu-id="52eb2-112">Dieser Befehl ruft alle Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="52eb2-112">This command gets all users.</span></span>

### <span data-ttu-id="52eb2-113">Beispiel 2: Abrufen eines Benutzers nach ID</span><span class="sxs-lookup"><span data-stu-id="52eb2-113">Example 2: Get a user by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="52eb2-114">Dieser Befehl ruft einen Benutzer nach ID ab.</span><span class="sxs-lookup"><span data-stu-id="52eb2-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="52eb2-115">Beispiel: Abrufen von Benutzern nach Nachname</span><span class="sxs-lookup"><span data-stu-id="52eb2-115">Example: Get users by last name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="52eb2-116">Mit diesem Befehl werden Benutzer mit dem angegebenen Nachnamen Fuller abgerufen.</span><span class="sxs-lookup"><span data-stu-id="52eb2-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="52eb2-117">Beispiel 4: Abrufen eines Benutzers per e-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="52eb2-117">Example 4: Get a user by email address</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="52eb2-118">Mit diesem Befehl wird der Benutzer mit der angegebenen e-Mail-Adresse abgerufen.</span><span class="sxs-lookup"><span data-stu-id="52eb2-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="52eb2-119">Beispiel 5: Abrufen aller Benutzer in einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="52eb2-119">Example 5: Get all users within a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="52eb2-120">Dieser Befehl ruft alle Benutzer in der angegebenen Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="52eb2-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="52eb2-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="52eb2-121">PARAMETERS</span></span>

### <span data-ttu-id="52eb2-122">-Context</span><span class="sxs-lookup"><span data-stu-id="52eb2-122">-Context</span></span>
<span data-ttu-id="52eb2-123">Gibt eine Instanz von **PsApiManagementContext** an.</span><span class="sxs-lookup"><span data-stu-id="52eb2-123">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="52eb2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52eb2-124">-DefaultProfile</span></span>
<span data-ttu-id="52eb2-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="52eb2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52eb2-126">– E-Mail</span><span class="sxs-lookup"><span data-stu-id="52eb2-126">-Email</span></span>
<span data-ttu-id="52eb2-127">Gibt die e-Mail-Adresse des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="52eb2-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="52eb2-128">Wenn dieser Parameter angegeben wird, findet ein Benutzer durch dieses Cmdlet eine e-Mail.</span><span class="sxs-lookup"><span data-stu-id="52eb2-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="52eb2-129">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="52eb2-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="52eb2-130">-FirstName</span><span class="sxs-lookup"><span data-stu-id="52eb2-130">-FirstName</span></span>
<span data-ttu-id="52eb2-131">Gibt den Vornamen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="52eb2-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="52eb2-132">Wenn dieser Parameter angegeben wird, findet dieses Cmdlet einen Benutzer mit dem Vornamen.</span><span class="sxs-lookup"><span data-stu-id="52eb2-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="52eb2-133">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="52eb2-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="52eb2-134">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="52eb2-134">-GroupId</span></span>
<span data-ttu-id="52eb2-135">Gibt die Gruppen-ID an.</span><span class="sxs-lookup"><span data-stu-id="52eb2-135">Specifies the group identifier.</span></span>
<span data-ttu-id="52eb2-136">Falls angegeben, findet dieses Cmdlet alle Benutzer in der angegebenen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="52eb2-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="52eb2-137">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="52eb2-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="52eb2-138">-Nachname</span><span class="sxs-lookup"><span data-stu-id="52eb2-138">-LastName</span></span>
<span data-ttu-id="52eb2-139">Gibt den letzten Namen eines Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="52eb2-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="52eb2-140">Falls angegeben, findet dieses Cmdlet Benutzer nach Nachname.</span><span class="sxs-lookup"><span data-stu-id="52eb2-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="52eb2-141">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="52eb2-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="52eb2-142">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="52eb2-142">-State</span></span>
<span data-ttu-id="52eb2-143">Gibt den Benutzerstatus an.</span><span class="sxs-lookup"><span data-stu-id="52eb2-143">Specifies the user state.</span></span>
<span data-ttu-id="52eb2-144">Falls angegeben, findet dieses Cmdlet Benutzer in diesem Zustand.</span><span class="sxs-lookup"><span data-stu-id="52eb2-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="52eb2-145">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="52eb2-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="52eb2-146">-UserID</span><span class="sxs-lookup"><span data-stu-id="52eb2-146">-UserId</span></span>
<span data-ttu-id="52eb2-147">Gibt eine Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="52eb2-147">Specifies a user ID.</span></span>
<span data-ttu-id="52eb2-148">Bei Angabe dieses Cmdlets findet der Benutzer diesen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="52eb2-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="52eb2-149">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="52eb2-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="52eb2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52eb2-150">CommonParameters</span></span>
<span data-ttu-id="52eb2-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52eb2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52eb2-152">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52eb2-152">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52eb2-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="52eb2-153">INPUTS</span></span>

### <span data-ttu-id="52eb2-154">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="52eb2-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="52eb2-155">System. String</span><span class="sxs-lookup"><span data-stu-id="52eb2-155">System.String</span></span>

### <span data-ttu-id="52eb2-156">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUserState, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. Servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="52eb2-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="52eb2-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="52eb2-157">OUTPUTS</span></span>

### <span data-ttu-id="52eb2-158">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="52eb2-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="52eb2-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="52eb2-159">NOTES</span></span>

## <span data-ttu-id="52eb2-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="52eb2-160">RELATED LINKS</span></span>

[<span data-ttu-id="52eb2-161">Neu – AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="52eb2-161">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="52eb2-162">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="52eb2-162">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)

[<span data-ttu-id="52eb2-163">Satz-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="52eb2-163">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


