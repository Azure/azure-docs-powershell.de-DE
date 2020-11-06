---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: 07f387239bdaad526c36c3928e7d2c5f490b0c7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483198"
---
# <span data-ttu-id="ee58b-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ee58b-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="ee58b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ee58b-102">SYNOPSIS</span></span>
<span data-ttu-id="ee58b-103">Ruft einen Benutzer oder Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="ee58b-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee58b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee58b-104">SYNTAX</span></span>

### <span data-ttu-id="ee58b-105">GeAllUsers (Standard)</span><span class="sxs-lookup"><span data-stu-id="ee58b-105">GeAllUsers (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ee58b-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="ee58b-106">GetByUserId</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee58b-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="ee58b-107">GetByUser</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee58b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee58b-108">DESCRIPTION</span></span>
<span data-ttu-id="ee58b-109">Das Cmdlet " **Get-AzureRmApiManagementUser** " Ruft einen angegebenen Benutzer oder alle Benutzer ab, wenn kein Benutzer angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ee58b-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="ee58b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ee58b-110">EXAMPLES</span></span>

### <span data-ttu-id="ee58b-111">Beispiel 1: Abrufen aller Benutzer</span><span class="sxs-lookup"><span data-stu-id="ee58b-111">Example 1: Get all users</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="ee58b-112">Dieser Befehl ruft alle Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="ee58b-112">This command gets all users.</span></span>

### <span data-ttu-id="ee58b-113">Beispiel 2: Abrufen eines Benutzers nach ID</span><span class="sxs-lookup"><span data-stu-id="ee58b-113">Example 2: Get a user by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="ee58b-114">Dieser Befehl ruft einen Benutzer nach ID ab.</span><span class="sxs-lookup"><span data-stu-id="ee58b-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="ee58b-115">Beispiel: Abrufen von Benutzern nach Nachname</span><span class="sxs-lookup"><span data-stu-id="ee58b-115">Example: Get users by last name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="ee58b-116">Mit diesem Befehl werden Benutzer mit dem angegebenen Nachnamen Fuller abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ee58b-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="ee58b-117">Beispiel 4: Abrufen eines Benutzers per e-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="ee58b-117">Example 4: Get a user by email address</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="ee58b-118">Mit diesem Befehl wird der Benutzer mit der angegebenen e-Mail-Adresse abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ee58b-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="ee58b-119">Beispiel 5: Abrufen aller Benutzer in einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="ee58b-119">Example 5: Get all users within a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="ee58b-120">Dieser Befehl ruft alle Benutzer in der angegebenen Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="ee58b-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="ee58b-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee58b-121">PARAMETERS</span></span>

### <span data-ttu-id="ee58b-122">-Context</span><span class="sxs-lookup"><span data-stu-id="ee58b-122">-Context</span></span>
<span data-ttu-id="ee58b-123">Gibt eine Instanz von **PsApiManagementContext** an.</span><span class="sxs-lookup"><span data-stu-id="ee58b-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee58b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee58b-124">-DefaultProfile</span></span>
<span data-ttu-id="ee58b-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ee58b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee58b-126">– E-Mail</span><span class="sxs-lookup"><span data-stu-id="ee58b-126">-Email</span></span>
<span data-ttu-id="ee58b-127">Gibt die e-Mail-Adresse des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="ee58b-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="ee58b-128">Wenn dieser Parameter angegeben wird, findet ein Benutzer durch dieses Cmdlet eine e-Mail.</span><span class="sxs-lookup"><span data-stu-id="ee58b-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="ee58b-129">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="ee58b-129">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee58b-130">-FirstName</span><span class="sxs-lookup"><span data-stu-id="ee58b-130">-FirstName</span></span>
<span data-ttu-id="ee58b-131">Gibt den Vornamen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="ee58b-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="ee58b-132">Wenn dieser Parameter angegeben wird, findet dieses Cmdlet einen Benutzer mit dem Vornamen.</span><span class="sxs-lookup"><span data-stu-id="ee58b-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="ee58b-133">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="ee58b-133">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee58b-134">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="ee58b-134">-GroupId</span></span>
<span data-ttu-id="ee58b-135">Gibt die Gruppen-ID an.</span><span class="sxs-lookup"><span data-stu-id="ee58b-135">Specifies the group identifier.</span></span>
<span data-ttu-id="ee58b-136">Falls angegeben, findet dieses Cmdlet alle Benutzer in der angegebenen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ee58b-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="ee58b-137">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="ee58b-137">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee58b-138">-Nachname</span><span class="sxs-lookup"><span data-stu-id="ee58b-138">-LastName</span></span>
<span data-ttu-id="ee58b-139">Gibt den letzten Namen eines Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="ee58b-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="ee58b-140">Falls angegeben, findet dieses Cmdlet Benutzer nach Nachname.</span><span class="sxs-lookup"><span data-stu-id="ee58b-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="ee58b-141">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="ee58b-141">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee58b-142">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="ee58b-142">-State</span></span>
<span data-ttu-id="ee58b-143">Gibt den Benutzerstatus an.</span><span class="sxs-lookup"><span data-stu-id="ee58b-143">Specifies the user state.</span></span>
<span data-ttu-id="ee58b-144">Falls angegeben, findet dieses Cmdlet Benutzer in diesem Zustand.</span><span class="sxs-lookup"><span data-stu-id="ee58b-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="ee58b-145">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="ee58b-145">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementUserState
Parameter Sets: GetByUser
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee58b-146">-UserID</span><span class="sxs-lookup"><span data-stu-id="ee58b-146">-UserId</span></span>
<span data-ttu-id="ee58b-147">Gibt eine Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="ee58b-147">Specifies a user ID.</span></span>
<span data-ttu-id="ee58b-148">Bei Angabe dieses Cmdlets findet der Benutzer diesen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="ee58b-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="ee58b-149">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="ee58b-149">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee58b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee58b-150">CommonParameters</span></span>
<span data-ttu-id="ee58b-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee58b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee58b-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee58b-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee58b-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ee58b-153">INPUTS</span></span>

### <span data-ttu-id="ee58b-154">Keine</span><span class="sxs-lookup"><span data-stu-id="ee58b-154">None</span></span>
<span data-ttu-id="ee58b-155">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ee58b-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ee58b-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ee58b-156">OUTPUTS</span></span>

### <span data-ttu-id="ee58b-157">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ee58b-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>
<span data-ttu-id="ee58b-158">Die Details des Benutzers im API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="ee58b-158">The details of User in API Management service.</span></span>

### <span data-ttu-id="ee58b-159">IList<Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUser></span><span class="sxs-lookup"><span data-stu-id="ee58b-159">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser></span></span>
<span data-ttu-id="ee58b-160">Die Liste der Benutzer im API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="ee58b-160">The list of User in the API Management  service.</span></span>

## <span data-ttu-id="ee58b-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="ee58b-161">NOTES</span></span>

## <span data-ttu-id="ee58b-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ee58b-162">RELATED LINKS</span></span>

[<span data-ttu-id="ee58b-163">Neu – AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ee58b-163">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="ee58b-164">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ee58b-164">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="ee58b-165">Satz-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ee58b-165">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


