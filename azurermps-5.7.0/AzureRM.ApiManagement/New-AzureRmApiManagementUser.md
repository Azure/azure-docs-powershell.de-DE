---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: fa7b44710aa51a138729d9a04a41a82ec2769f5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665335"
---
# <span data-ttu-id="e5d87-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e5d87-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="e5d87-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5d87-102">SYNOPSIS</span></span>
<span data-ttu-id="e5d87-103">Registriert einen neuen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="e5d87-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5d87-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5d87-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5d87-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5d87-105">DESCRIPTION</span></span>
<span data-ttu-id="e5d87-106">Das Cmdlet **New-AzureRmApiManagementUser** registriert einen neuen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="e5d87-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="e5d87-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5d87-107">EXAMPLES</span></span>

### <span data-ttu-id="e5d87-108">Beispiel 1: Registrieren eines neuen Benutzers</span><span class="sxs-lookup"><span data-stu-id="e5d87-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="e5d87-109">Mit diesem Befehl wird ein neuer Benutzernamens Patti Fuller registriert.</span><span class="sxs-lookup"><span data-stu-id="e5d87-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="e5d87-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5d87-110">PARAMETERS</span></span>

### <span data-ttu-id="e5d87-111">-Context</span><span class="sxs-lookup"><span data-stu-id="e5d87-111">-Context</span></span>
<span data-ttu-id="e5d87-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e5d87-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e5d87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5d87-113">-DefaultProfile</span></span>
<span data-ttu-id="e5d87-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5d87-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="e5d87-115">– E-Mail</span><span class="sxs-lookup"><span data-stu-id="e5d87-115">-Email</span></span>
<span data-ttu-id="e5d87-116">Gibt die e-Mail-Adresse des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="e5d87-116">Specifies the email address of the user.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5d87-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="e5d87-117">-FirstName</span></span>
<span data-ttu-id="e5d87-118">Gibt den Vornamen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="e5d87-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="e5d87-119">Dieser Parameter muss 1 bis 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="e5d87-119">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5d87-120">-Nachname</span><span class="sxs-lookup"><span data-stu-id="e5d87-120">-LastName</span></span>
<span data-ttu-id="e5d87-121">Gibt den letzten Namen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="e5d87-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="e5d87-122">Dieser Parameter muss 1 bis 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="e5d87-122">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5d87-123">-Hinweis</span><span class="sxs-lookup"><span data-stu-id="e5d87-123">-Note</span></span>
<span data-ttu-id="e5d87-124">Gibt eine Notiz über den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="e5d87-124">Specifies a note about the user.</span></span>
<span data-ttu-id="e5d87-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e5d87-125">This parameter is optional.</span></span>
<span data-ttu-id="e5d87-126">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="e5d87-126">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5d87-127">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="e5d87-127">-Password</span></span>
<span data-ttu-id="e5d87-128">Gibt das Benutzerkennwort an.</span><span class="sxs-lookup"><span data-stu-id="e5d87-128">Specifies the user password.</span></span>
<span data-ttu-id="e5d87-129">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e5d87-129">This parameter is required.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5d87-130">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="e5d87-130">-State</span></span>
<span data-ttu-id="e5d87-131">Gibt den Benutzerstatus an.</span><span class="sxs-lookup"><span data-stu-id="e5d87-131">Specifies the user state.</span></span>
<span data-ttu-id="e5d87-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e5d87-132">This parameter is optional.</span></span>
<span data-ttu-id="e5d87-133">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="e5d87-133">The default value of this parameter is $Null.</span></span>

```yaml
Type: PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5d87-134">-UserID</span><span class="sxs-lookup"><span data-stu-id="e5d87-134">-UserId</span></span>
<span data-ttu-id="e5d87-135">Gibt die Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="e5d87-135">Specifies the user ID.</span></span>
<span data-ttu-id="e5d87-136">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e5d87-136">This parameter is optional.</span></span>
<span data-ttu-id="e5d87-137">Wenn dieser Parameter nicht angegeben wird, generiert dieses Cmdlet eine Benutzer-ID.</span><span class="sxs-lookup"><span data-stu-id="e5d87-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5d87-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5d87-138">CommonParameters</span></span>
<span data-ttu-id="e5d87-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5d87-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5d87-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5d87-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5d87-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5d87-141">INPUTS</span></span>

### <span data-ttu-id="e5d87-142">Keine</span><span class="sxs-lookup"><span data-stu-id="e5d87-142">None</span></span>
<span data-ttu-id="e5d87-143">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="e5d87-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e5d87-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5d87-144">OUTPUTS</span></span>

### <span data-ttu-id="e5d87-145">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e5d87-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="e5d87-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5d87-146">NOTES</span></span>

## <span data-ttu-id="e5d87-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5d87-147">RELATED LINKS</span></span>

[<span data-ttu-id="e5d87-148">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e5d87-148">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="e5d87-149">Satz-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e5d87-149">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


