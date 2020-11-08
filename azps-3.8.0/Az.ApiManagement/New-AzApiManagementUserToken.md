---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementusertoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
ms.openlocfilehash: 5b8c781380ced5ed174c094cf1ff66a8eb820309
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996623"
---
# <span data-ttu-id="b0fca-101">New-AzApiManagementUserToken</span><span class="sxs-lookup"><span data-stu-id="b0fca-101">New-AzApiManagementUserToken</span></span>

## <span data-ttu-id="b0fca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b0fca-102">SYNOPSIS</span></span>
<span data-ttu-id="b0fca-103">Generiert ein freigegebenes Zugriffs Token für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b0fca-103">Generates a Shared Access Token for the User.</span></span>

## <span data-ttu-id="b0fca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0fca-104">SYNTAX</span></span>

```
New-AzApiManagementUserToken -Context <PsApiManagementContext> -UserId <String>
 [-KeyType <PsApiManagementUserKeyType>] [-Expiry <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0fca-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0fca-105">DESCRIPTION</span></span>
<span data-ttu-id="b0fca-106">Das Cmdlet **New-AzApiManagementUserToken** generiert ein freigegebenes Zugriffs Token für einen angegebenen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b0fca-106">The cmdlet **New-AzApiManagementUserToken** generates a Shared Access Token for a specified User</span></span>

## <span data-ttu-id="b0fca-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0fca-107">EXAMPLES</span></span>

### <span data-ttu-id="b0fca-108">Beispiel 1: Generieren eines freigegebenen Zugriffstokens für git-Benutzer</span><span class="sxs-lookup"><span data-stu-id="b0fca-108">Example 1 : Generate a Shared Access Token for Git User</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName powershelltest -ServiceName
powershellsdkservice
S D:\github\azure-powershell> $gitAccess=Get-AzApiManagementTenantAccess -Context $context
PS D:\github\azure-powershell> New-AzApiManagementUserToken -Context $context -UserId $gitAccess.Id

UserId      TokenExpiry         KeyType UserToken
------      -----------         ------- ---------
integration 5/3/2019 2:02:34 PM Primary integration&201905031402&zOwopJChWAA6oaqGHMyf7Ol9wUCPcrtdmBmff8c2lcmZk9Y...
```

<span data-ttu-id="b0fca-109">Dieses Skript ruft den im ApiManagement-Dienst konfigurierten git-Benutzer ab und generiert mithilfe des Primärschlüssels, der für 8 Stunden gültig ist, ein freigegebenes Zugriffs Token.</span><span class="sxs-lookup"><span data-stu-id="b0fca-109">This script get the Git user configured in ApiManagement service and generates a Shared Access Token using the Primary Key valid for 8 hours.</span></span>

## <span data-ttu-id="b0fca-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0fca-110">PARAMETERS</span></span>

### <span data-ttu-id="b0fca-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b0fca-111">-Context</span></span>
<span data-ttu-id="b0fca-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b0fca-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b0fca-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b0fca-113">This parameter is required.</span></span>

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

### <span data-ttu-id="b0fca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0fca-114">-DefaultProfile</span></span>
<span data-ttu-id="b0fca-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b0fca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0fca-116">-Ablauf</span><span class="sxs-lookup"><span data-stu-id="b0fca-116">-Expiry</span></span>
<span data-ttu-id="b0fca-117">Ablauf des Tokens.</span><span class="sxs-lookup"><span data-stu-id="b0fca-117">Expiry of the Token.</span></span>
<span data-ttu-id="b0fca-118">Wenn Sie nicht angegeben wird, wird das Token erstellt, um nach 8 Stunden zu verfallen.</span><span class="sxs-lookup"><span data-stu-id="b0fca-118">If not specified, the token is created to expire after 8 hours.</span></span>
<span data-ttu-id="b0fca-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="b0fca-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="b0fca-120">-KeyType</span><span class="sxs-lookup"><span data-stu-id="b0fca-120">-KeyType</span></span>
<span data-ttu-id="b0fca-121">Der beim Generieren des Tokens zu verwendende Benutzerschlüssel.</span><span class="sxs-lookup"><span data-stu-id="b0fca-121">User Key to use when generating the Token.</span></span>
<span data-ttu-id="b0fca-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="b0fca-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="b0fca-123">-UserID</span><span class="sxs-lookup"><span data-stu-id="b0fca-123">-UserId</span></span>
<span data-ttu-id="b0fca-124">Bezeichner eines vorhandenen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="b0fca-124">Identifier of existing user.</span></span>
<span data-ttu-id="b0fca-125">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b0fca-125">This parameter is required.</span></span>

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

### <span data-ttu-id="b0fca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0fca-126">CommonParameters</span></span>
<span data-ttu-id="b0fca-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0fca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0fca-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0fca-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0fca-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b0fca-129">INPUTS</span></span>

### <span data-ttu-id="b0fca-130">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b0fca-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b0fca-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b0fca-131">System.String</span></span>

### <span data-ttu-id="b0fca-132">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUserKeyType</span><span class="sxs-lookup"><span data-stu-id="b0fca-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserKeyType</span></span>

### <span data-ttu-id="b0fca-133">System. Nullable ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b0fca-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b0fca-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b0fca-134">OUTPUTS</span></span>

### <span data-ttu-id="b0fca-135">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUserToken</span><span class="sxs-lookup"><span data-stu-id="b0fca-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserToken</span></span>

## <span data-ttu-id="b0fca-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="b0fca-136">NOTES</span></span>

## <span data-ttu-id="b0fca-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b0fca-137">RELATED LINKS</span></span>
