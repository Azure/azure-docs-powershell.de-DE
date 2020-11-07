---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementusertoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
ms.openlocfilehash: 71f4960dce883b809d9ee9c5bc7011d8ab04c5bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658222"
---
# <span data-ttu-id="a38a5-101">New-AzApiManagementUserToken</span><span class="sxs-lookup"><span data-stu-id="a38a5-101">New-AzApiManagementUserToken</span></span>

## <span data-ttu-id="a38a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a38a5-102">SYNOPSIS</span></span>
<span data-ttu-id="a38a5-103">Generiert ein freigegebenes Zugriffs Token für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="a38a5-103">Generates a Shared Access Token for the User.</span></span>

## <span data-ttu-id="a38a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a38a5-104">SYNTAX</span></span>

```
New-AzApiManagementUserToken -Context <PsApiManagementContext> -UserId <String>
 [-KeyType <PsApiManagementUserKeyType>] [-Expiry <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a38a5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a38a5-105">DESCRIPTION</span></span>
<span data-ttu-id="a38a5-106">Das Cmdlet **New-AzApiManagementUserToken** generiert ein freigegebenes Zugriffs Token für einen angegebenen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="a38a5-106">The cmdlet **New-AzApiManagementUserToken** generates a Shared Access Token for a specified User</span></span>

## <span data-ttu-id="a38a5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a38a5-107">EXAMPLES</span></span>

### <span data-ttu-id="a38a5-108">Beispiel 1: Generieren eines freigegebenen Zugriffstokens für git-Benutzer</span><span class="sxs-lookup"><span data-stu-id="a38a5-108">Example 1 : Generate a Shared Access Token for Git User</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName powershelltest -ServiceName
powershellsdkservice
S D:\github\azure-powershell> $gitAccess=Get-AzApiManagementTenantAccess -Context $context
PS D:\github\azure-powershell> New-AzApiManagementUserToken -Context $context -UserId $gitAccess.Id

UserId      TokenExpiry         KeyType UserToken
------      -----------         ------- ---------
integration 5/3/2019 2:02:34 PM Primary integration&201905031402&zOwopJChWAA6oaqGHMyf7Ol9wUCPcrtdmBmff8c2lcmZk9Y...
```

<span data-ttu-id="a38a5-109">Dieses Skript ruft den im ApiManagement-Dienst konfigurierten git-Benutzer ab und generiert mithilfe des Primärschlüssels, der für 8 Stunden gültig ist, ein freigegebenes Zugriffs Token.</span><span class="sxs-lookup"><span data-stu-id="a38a5-109">This script get the Git user configured in ApiManagement service and generates a Shared Access Token using the Primary Key valid for 8 hours.</span></span>

## <span data-ttu-id="a38a5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a38a5-110">PARAMETERS</span></span>

### <span data-ttu-id="a38a5-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a38a5-111">-Context</span></span>
<span data-ttu-id="a38a5-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a38a5-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a38a5-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a38a5-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a38a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a38a5-114">-DefaultProfile</span></span>
<span data-ttu-id="a38a5-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a38a5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a38a5-116">-Ablauf</span><span class="sxs-lookup"><span data-stu-id="a38a5-116">-Expiry</span></span>
<span data-ttu-id="a38a5-117">Ablauf des Tokens.</span><span class="sxs-lookup"><span data-stu-id="a38a5-117">Expiry of the Token.</span></span>
<span data-ttu-id="a38a5-118">Wenn Sie nicht angegeben wird, wird das Token erstellt, um nach 8 Stunden zu verfallen.</span><span class="sxs-lookup"><span data-stu-id="a38a5-118">If not specified, the token is created to expire after 8 hours.</span></span>
<span data-ttu-id="a38a5-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a38a5-119">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a38a5-120">-KeyType</span><span class="sxs-lookup"><span data-stu-id="a38a5-120">-KeyType</span></span>
<span data-ttu-id="a38a5-121">Der beim Generieren des Tokens zu verwendende Benutzerschlüssel.</span><span class="sxs-lookup"><span data-stu-id="a38a5-121">User Key to use when generating the Token.</span></span>
<span data-ttu-id="a38a5-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a38a5-122">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserKeyType
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a38a5-123">-UserID</span><span class="sxs-lookup"><span data-stu-id="a38a5-123">-UserId</span></span>
<span data-ttu-id="a38a5-124">Bezeichner eines vorhandenen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="a38a5-124">Identifier of existing user.</span></span>
<span data-ttu-id="a38a5-125">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a38a5-125">This parameter is required.</span></span>

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

### <span data-ttu-id="a38a5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a38a5-126">CommonParameters</span></span>
<span data-ttu-id="a38a5-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a38a5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a38a5-128">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a38a5-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a38a5-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a38a5-129">INPUTS</span></span>

### <span data-ttu-id="a38a5-130">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a38a5-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a38a5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a38a5-131">System.String</span></span>

### <span data-ttu-id="a38a5-132">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUserKeyType</span><span class="sxs-lookup"><span data-stu-id="a38a5-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserKeyType</span></span>

### <span data-ttu-id="a38a5-133">System. Nullable ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a38a5-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a38a5-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a38a5-134">OUTPUTS</span></span>

### <span data-ttu-id="a38a5-135">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUserToken</span><span class="sxs-lookup"><span data-stu-id="a38a5-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserToken</span></span>

## <span data-ttu-id="a38a5-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="a38a5-136">NOTES</span></span>

## <span data-ttu-id="a38a5-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a38a5-137">RELATED LINKS</span></span>
