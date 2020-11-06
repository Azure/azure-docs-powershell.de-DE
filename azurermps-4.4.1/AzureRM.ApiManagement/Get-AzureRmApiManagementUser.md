---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: be6c9ee6c0db12e324786052348209703b79601e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477449"
---
# <span data-ttu-id="815e7-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="815e7-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="815e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="815e7-102">SYNOPSIS</span></span>
<span data-ttu-id="815e7-103">Ruft einen Benutzer oder Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="815e7-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="815e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="815e7-104">SYNTAX</span></span>

### <span data-ttu-id="815e7-105">Alle Benutzer abrufen (Standard)</span><span class="sxs-lookup"><span data-stu-id="815e7-105">Get all users (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="815e7-106">Benutzer nach ID abrufen</span><span class="sxs-lookup"><span data-stu-id="815e7-106">Get user by ID</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="815e7-107">Suchen von Benutzern</span><span class="sxs-lookup"><span data-stu-id="815e7-107">Find users</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="815e7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="815e7-108">DESCRIPTION</span></span>
<span data-ttu-id="815e7-109">Das Cmdlet " **Get-AzureRmApiManagementUser** " Ruft einen angegebenen Benutzer oder alle Benutzer ab, wenn kein Benutzer angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="815e7-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="815e7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="815e7-110">EXAMPLES</span></span>

### <span data-ttu-id="815e7-111">Beispiel 1: Abrufen aller Benutzer</span><span class="sxs-lookup"><span data-stu-id="815e7-111">Example 1: Get all users</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="815e7-112">Dieser Befehl ruft alle Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="815e7-112">This command gets all users.</span></span>

### <span data-ttu-id="815e7-113">Beispiel 2: Abrufen eines Benutzers nach ID</span><span class="sxs-lookup"><span data-stu-id="815e7-113">Example 2: Get a user by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="815e7-114">Dieser Befehl ruft einen Benutzer nach ID ab.</span><span class="sxs-lookup"><span data-stu-id="815e7-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="815e7-115">Beispiel: Abrufen von Benutzern nach Nachname</span><span class="sxs-lookup"><span data-stu-id="815e7-115">Example: Get users by last name</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="815e7-116">Mit diesem Befehl werden Benutzer mit dem angegebenen Nachnamen Fuller abgerufen.</span><span class="sxs-lookup"><span data-stu-id="815e7-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="815e7-117">Beispiel 4: Abrufen eines Benutzers per e-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="815e7-117">Example 4: Get a user by email address</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email 
"user@contoso.com"
```

<span data-ttu-id="815e7-118">Mit diesem Befehl wird der Benutzer mit der angegebenen e-Mail-Adresse abgerufen.</span><span class="sxs-lookup"><span data-stu-id="815e7-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="815e7-119">Beispiel 5: Abrufen aller Benutzer in einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="815e7-119">Example 5: Get all users within a group</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="815e7-120">Dieser Befehl ruft alle Benutzer in der angegebenen Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="815e7-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="815e7-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="815e7-121">PARAMETERS</span></span>

### <span data-ttu-id="815e7-122">-Context</span><span class="sxs-lookup"><span data-stu-id="815e7-122">-Context</span></span>
<span data-ttu-id="815e7-123">Gibt eine Instanz von **PsApiManagementContext** an.</span><span class="sxs-lookup"><span data-stu-id="815e7-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="815e7-124">– E-Mail</span><span class="sxs-lookup"><span data-stu-id="815e7-124">-Email</span></span>
<span data-ttu-id="815e7-125">Gibt die e-Mail-Adresse des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="815e7-125">Specifies the email address of the user.</span></span>
<span data-ttu-id="815e7-126">Wenn dieser Parameter angegeben wird, findet ein Benutzer durch dieses Cmdlet eine e-Mail.</span><span class="sxs-lookup"><span data-stu-id="815e7-126">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="815e7-127">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="815e7-127">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="815e7-128">-FirstName</span><span class="sxs-lookup"><span data-stu-id="815e7-128">-FirstName</span></span>
<span data-ttu-id="815e7-129">Gibt den Vornamen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="815e7-129">Specifies the first name of the user.</span></span>
<span data-ttu-id="815e7-130">Wenn dieser Parameter angegeben wird, findet dieses Cmdlet einen Benutzer mit dem Vornamen.</span><span class="sxs-lookup"><span data-stu-id="815e7-130">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="815e7-131">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="815e7-131">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="815e7-132">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="815e7-132">-GroupId</span></span>
<span data-ttu-id="815e7-133">Gibt die Gruppen-ID an.</span><span class="sxs-lookup"><span data-stu-id="815e7-133">Specifies the group identifier.</span></span>
<span data-ttu-id="815e7-134">Falls angegeben, findet dieses Cmdlet alle Benutzer in der angegebenen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="815e7-134">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="815e7-135">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="815e7-135">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="815e7-136">-Nachname</span><span class="sxs-lookup"><span data-stu-id="815e7-136">-LastName</span></span>
<span data-ttu-id="815e7-137">Gibt den letzten Namen eines Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="815e7-137">Specifies the last name of a user.</span></span>
<span data-ttu-id="815e7-138">Falls angegeben, findet dieses Cmdlet Benutzer nach Nachname.</span><span class="sxs-lookup"><span data-stu-id="815e7-138">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="815e7-139">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="815e7-139">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="815e7-140">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="815e7-140">-State</span></span>
<span data-ttu-id="815e7-141">Gibt den Benutzerstatus an.</span><span class="sxs-lookup"><span data-stu-id="815e7-141">Specifies the user state.</span></span>
<span data-ttu-id="815e7-142">Falls angegeben, findet dieses Cmdlet Benutzer in diesem Zustand.</span><span class="sxs-lookup"><span data-stu-id="815e7-142">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="815e7-143">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="815e7-143">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: Find users
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="815e7-144">-UserID</span><span class="sxs-lookup"><span data-stu-id="815e7-144">-UserId</span></span>
<span data-ttu-id="815e7-145">Gibt eine Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="815e7-145">Specifies a user ID.</span></span>
<span data-ttu-id="815e7-146">Bei Angabe dieses Cmdlets findet der Benutzer diesen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="815e7-146">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="815e7-147">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="815e7-147">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Get user by ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="815e7-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="815e7-148">-DefaultProfile</span></span>
<span data-ttu-id="815e7-149">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="815e7-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="815e7-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="815e7-150">CommonParameters</span></span>
<span data-ttu-id="815e7-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="815e7-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="815e7-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="815e7-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="815e7-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="815e7-153">INPUTS</span></span>

## <span data-ttu-id="815e7-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="815e7-154">OUTPUTS</span></span>

### <span data-ttu-id="815e7-155">IList<Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUser></span><span class="sxs-lookup"><span data-stu-id="815e7-155">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser></span></span>

## <span data-ttu-id="815e7-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="815e7-156">NOTES</span></span>

## <span data-ttu-id="815e7-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="815e7-157">RELATED LINKS</span></span>

[<span data-ttu-id="815e7-158">Neu – AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="815e7-158">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="815e7-159">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="815e7-159">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="815e7-160">Satz-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="815e7-160">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


