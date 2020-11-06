---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: 93e6ce5a96afd1c3b297d6296c3491445593d430
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499278"
---
# <span data-ttu-id="870a5-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="870a5-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="870a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="870a5-102">SYNOPSIS</span></span>
<span data-ttu-id="870a5-103">Registriert einen neuen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="870a5-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="870a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="870a5-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <String> [-State <PsApiManagementUserState>] [-Note <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="870a5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="870a5-105">DESCRIPTION</span></span>
<span data-ttu-id="870a5-106">Das Cmdlet **New-AzureRmApiManagementUser** registriert einen neuen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="870a5-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="870a5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="870a5-107">EXAMPLES</span></span>

### <span data-ttu-id="870a5-108">Beispiel 1: Registrieren eines neuen Benutzers</span><span class="sxs-lookup"><span data-stu-id="870a5-108">Example 1: Register a new user</span></span>
```
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password "qwerty"
```

<span data-ttu-id="870a5-109">Mit diesem Befehl wird ein neuer Benutzernamens Patti Fuller registriert.</span><span class="sxs-lookup"><span data-stu-id="870a5-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="870a5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="870a5-110">PARAMETERS</span></span>

### <span data-ttu-id="870a5-111">-Context</span><span class="sxs-lookup"><span data-stu-id="870a5-111">-Context</span></span>
<span data-ttu-id="870a5-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="870a5-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="870a5-113">– E-Mail</span><span class="sxs-lookup"><span data-stu-id="870a5-113">-Email</span></span>
<span data-ttu-id="870a5-114">Gibt die e-Mail-Adresse des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="870a5-114">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="870a5-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="870a5-115">-FirstName</span></span>
<span data-ttu-id="870a5-116">Gibt den Vornamen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="870a5-116">Specifies the first name of the user.</span></span>
<span data-ttu-id="870a5-117">Dieser Parameter muss 1 bis 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="870a5-117">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="870a5-118">-Nachname</span><span class="sxs-lookup"><span data-stu-id="870a5-118">-LastName</span></span>
<span data-ttu-id="870a5-119">Gibt den letzten Namen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="870a5-119">Specifies the last name of the user.</span></span>
<span data-ttu-id="870a5-120">Dieser Parameter muss 1 bis 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="870a5-120">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="870a5-121">-Hinweis</span><span class="sxs-lookup"><span data-stu-id="870a5-121">-Note</span></span>
<span data-ttu-id="870a5-122">Gibt eine Notiz über den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="870a5-122">Specifies a note about the user.</span></span>
<span data-ttu-id="870a5-123">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="870a5-123">This parameter is optional.</span></span>
<span data-ttu-id="870a5-124">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="870a5-124">The default value is $Null.</span></span>

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

### <span data-ttu-id="870a5-125">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="870a5-125">-Password</span></span>
<span data-ttu-id="870a5-126">Gibt das Benutzerkennwort an.</span><span class="sxs-lookup"><span data-stu-id="870a5-126">Specifies the user password.</span></span>
<span data-ttu-id="870a5-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="870a5-127">This parameter is required.</span></span>

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

### <span data-ttu-id="870a5-128">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="870a5-128">-State</span></span>
<span data-ttu-id="870a5-129">Gibt den Benutzerstatus an.</span><span class="sxs-lookup"><span data-stu-id="870a5-129">Specifies the user state.</span></span>
<span data-ttu-id="870a5-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="870a5-130">This parameter is optional.</span></span>
<span data-ttu-id="870a5-131">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="870a5-131">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="870a5-132">-UserID</span><span class="sxs-lookup"><span data-stu-id="870a5-132">-UserId</span></span>
<span data-ttu-id="870a5-133">Gibt die Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="870a5-133">Specifies the user ID.</span></span>
<span data-ttu-id="870a5-134">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="870a5-134">This parameter is optional.</span></span>
<span data-ttu-id="870a5-135">Wenn dieser Parameter nicht angegeben wird, generiert dieses Cmdlet eine Benutzer-ID.</span><span class="sxs-lookup"><span data-stu-id="870a5-135">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="870a5-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="870a5-136">-DefaultProfile</span></span>
<span data-ttu-id="870a5-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="870a5-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="870a5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="870a5-138">CommonParameters</span></span>
<span data-ttu-id="870a5-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="870a5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="870a5-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="870a5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="870a5-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="870a5-141">INPUTS</span></span>

## <span data-ttu-id="870a5-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="870a5-142">OUTPUTS</span></span>

### <span data-ttu-id="870a5-143">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="870a5-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="870a5-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="870a5-144">NOTES</span></span>

## <span data-ttu-id="870a5-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="870a5-145">RELATED LINKS</span></span>

[<span data-ttu-id="870a5-146">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="870a5-146">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="870a5-147">Satz-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="870a5-147">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


