---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 30ff5f7d9ead2226c6c03b4707af9c20ff40d405
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821128"
---
# <span data-ttu-id="bc0b7-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="bc0b7-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="bc0b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bc0b7-102">SYNOPSIS</span></span>
<span data-ttu-id="bc0b7-103">Registriert einen neuen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-103">Registers a new user.</span></span>

## <span data-ttu-id="bc0b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc0b7-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc0b7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc0b7-105">DESCRIPTION</span></span>
<span data-ttu-id="bc0b7-106">Das Cmdlet **New-AzApiManagementUser** registriert einen neuen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="bc0b7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc0b7-107">EXAMPLES</span></span>

### <span data-ttu-id="bc0b7-108">Beispiel 1: Registrieren eines neuen Benutzers</span><span class="sxs-lookup"><span data-stu-id="bc0b7-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="bc0b7-109">Mit diesem Befehl wird ein neuer Benutzernamens Patti Fuller registriert.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="bc0b7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc0b7-110">PARAMETERS</span></span>

### <span data-ttu-id="bc0b7-111">-Context</span><span class="sxs-lookup"><span data-stu-id="bc0b7-111">-Context</span></span>
<span data-ttu-id="bc0b7-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bc0b7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc0b7-113">-DefaultProfile</span></span>
<span data-ttu-id="bc0b7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc0b7-115">– E-Mail</span><span class="sxs-lookup"><span data-stu-id="bc0b7-115">-Email</span></span>
<span data-ttu-id="bc0b7-116">Gibt die e-Mail-Adresse des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="bc0b7-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="bc0b7-117">-FirstName</span></span>
<span data-ttu-id="bc0b7-118">Gibt den Vornamen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="bc0b7-119">Dieser Parameter muss 1 bis 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="bc0b7-120">-Nachname</span><span class="sxs-lookup"><span data-stu-id="bc0b7-120">-LastName</span></span>
<span data-ttu-id="bc0b7-121">Gibt den letzten Namen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="bc0b7-122">Dieser Parameter muss 1 bis 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="bc0b7-123">-Hinweis</span><span class="sxs-lookup"><span data-stu-id="bc0b7-123">-Note</span></span>
<span data-ttu-id="bc0b7-124">Gibt eine Notiz über den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-124">Specifies a note about the user.</span></span>
<span data-ttu-id="bc0b7-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-125">This parameter is optional.</span></span>
<span data-ttu-id="bc0b7-126">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="bc0b7-127">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="bc0b7-127">-Password</span></span>
<span data-ttu-id="bc0b7-128">Gibt das Benutzerkennwort an.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-128">Specifies the user password.</span></span>
<span data-ttu-id="bc0b7-129">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-129">This parameter is required.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc0b7-130">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="bc0b7-130">-State</span></span>
<span data-ttu-id="bc0b7-131">Gibt den Benutzerstatus an.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-131">Specifies the user state.</span></span>
<span data-ttu-id="bc0b7-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-132">This parameter is optional.</span></span>
<span data-ttu-id="bc0b7-133">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-133">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc0b7-134">-UserID</span><span class="sxs-lookup"><span data-stu-id="bc0b7-134">-UserId</span></span>
<span data-ttu-id="bc0b7-135">Gibt die Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-135">Specifies the user ID.</span></span>
<span data-ttu-id="bc0b7-136">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-136">This parameter is optional.</span></span>
<span data-ttu-id="bc0b7-137">Wenn dieser Parameter nicht angegeben wird, generiert dieses Cmdlet eine Benutzer-ID.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="bc0b7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc0b7-138">CommonParameters</span></span>
<span data-ttu-id="bc0b7-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc0b7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc0b7-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc0b7-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc0b7-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bc0b7-141">INPUTS</span></span>

### <span data-ttu-id="bc0b7-142">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bc0b7-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bc0b7-143">System. String</span><span class="sxs-lookup"><span data-stu-id="bc0b7-143">System.String</span></span>

### <span data-ttu-id="bc0b7-144">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="bc0b7-144">System.Security.SecureString</span></span>

### <span data-ttu-id="bc0b7-145">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUserState, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. Servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bc0b7-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="bc0b7-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bc0b7-146">OUTPUTS</span></span>

### <span data-ttu-id="bc0b7-147">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="bc0b7-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="bc0b7-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="bc0b7-148">NOTES</span></span>

## <span data-ttu-id="bc0b7-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bc0b7-149">RELATED LINKS</span></span>

[<span data-ttu-id="bc0b7-150">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="bc0b7-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="bc0b7-151">Satz-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="bc0b7-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


