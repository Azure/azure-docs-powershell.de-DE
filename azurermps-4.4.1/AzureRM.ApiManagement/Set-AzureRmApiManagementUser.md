---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: a9d36dca9894a10c76f2ca5a96880f4aafecb5e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477394"
---
# <span data-ttu-id="1fa23-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1fa23-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="1fa23-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1fa23-102">SYNOPSIS</span></span>
<span data-ttu-id="1fa23-103">Legt Benutzer Details fest.</span><span class="sxs-lookup"><span data-stu-id="1fa23-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fa23-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fa23-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <String>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fa23-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1fa23-105">DESCRIPTION</span></span>
<span data-ttu-id="1fa23-106">Das Cmdlet " **Set-AzureRmApiManagementUser** " legt Benutzer Details fest.</span><span class="sxs-lookup"><span data-stu-id="1fa23-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="1fa23-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1fa23-107">EXAMPLES</span></span>

### <span data-ttu-id="1fa23-108">Beispiel 1: Ändern des Kennworts, der e-Mail-Adresse und des Status eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="1fa23-108">Example 1: Change a user's password, email address and state</span></span>
```
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password "asdfgh" -State "Blocked"
```

<span data-ttu-id="1fa23-109">Mit diesem Befehl wird ein neues Benutzerkennwort und eine e-Mail-Adresse festgelegt und der Benutzer blockiert.</span><span class="sxs-lookup"><span data-stu-id="1fa23-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="1fa23-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fa23-110">PARAMETERS</span></span>

### <span data-ttu-id="1fa23-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1fa23-111">-Context</span></span>
<span data-ttu-id="1fa23-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="1fa23-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="1fa23-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1fa23-113">This parameter is required.</span></span>

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

### <span data-ttu-id="1fa23-114">– E-Mail</span><span class="sxs-lookup"><span data-stu-id="1fa23-114">-Email</span></span>
<span data-ttu-id="1fa23-115">Gibt die e-Mail-Adresse des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="1fa23-115">Specifies the email address of the user.</span></span>
<span data-ttu-id="1fa23-116">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="1fa23-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fa23-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="1fa23-117">-FirstName</span></span>
<span data-ttu-id="1fa23-118">Gibt den Vornamen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="1fa23-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="1fa23-119">Dieser Parameter muss 1 bis 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="1fa23-119">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fa23-120">-Nachname</span><span class="sxs-lookup"><span data-stu-id="1fa23-120">-LastName</span></span>
<span data-ttu-id="1fa23-121">Gibt den letzten Namen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="1fa23-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="1fa23-122">Dieser Parameter muss 1 bis 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="1fa23-122">This parameter is must be 1 to 100 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fa23-123">-Hinweis</span><span class="sxs-lookup"><span data-stu-id="1fa23-123">-Note</span></span>
<span data-ttu-id="1fa23-124">Gibt eine Notiz über den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="1fa23-124">Specifies a note about the user.</span></span>
<span data-ttu-id="1fa23-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="1fa23-125">This parameter is optional.</span></span>
<span data-ttu-id="1fa23-126">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="1fa23-126">The default value of this parameter is $null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fa23-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fa23-127">-PassThru</span></span>
<span data-ttu-id="1fa23-128">passthru</span><span class="sxs-lookup"><span data-stu-id="1fa23-128">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fa23-129">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="1fa23-129">-Password</span></span>
<span data-ttu-id="1fa23-130">Gibt das Benutzerkennwort an.</span><span class="sxs-lookup"><span data-stu-id="1fa23-130">Specifies the user password.</span></span>
<span data-ttu-id="1fa23-131">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="1fa23-131">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fa23-132">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="1fa23-132">-State</span></span>
<span data-ttu-id="1fa23-133">Gibt den Benutzerstatus an.</span><span class="sxs-lookup"><span data-stu-id="1fa23-133">Specifies the user state.</span></span>
<span data-ttu-id="1fa23-134">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="1fa23-134">This parameter is optional.</span></span>
<span data-ttu-id="1fa23-135">Der Standardwert ist aktiv.</span><span class="sxs-lookup"><span data-stu-id="1fa23-135">The default value is Active.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fa23-136">-UserID</span><span class="sxs-lookup"><span data-stu-id="1fa23-136">-UserId</span></span>
<span data-ttu-id="1fa23-137">Gibt die Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="1fa23-137">Specifies the user ID.</span></span>
<span data-ttu-id="1fa23-138">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1fa23-138">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fa23-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fa23-139">-DefaultProfile</span></span>
<span data-ttu-id="1fa23-140">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1fa23-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fa23-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fa23-141">CommonParameters</span></span>
<span data-ttu-id="1fa23-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fa23-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fa23-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fa23-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fa23-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1fa23-144">INPUTS</span></span>

## <span data-ttu-id="1fa23-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1fa23-145">OUTPUTS</span></span>

### <span data-ttu-id="1fa23-146">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1fa23-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="1fa23-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="1fa23-147">NOTES</span></span>

## <span data-ttu-id="1fa23-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1fa23-148">RELATED LINKS</span></span>

[<span data-ttu-id="1fa23-149">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1fa23-149">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="1fa23-150">Neu – AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1fa23-150">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="1fa23-151">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1fa23-151">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


