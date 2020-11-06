---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 16a48b6f945aac8ef287ff612d64da1273add521
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477434"
---
# <span data-ttu-id="03fd6-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="03fd6-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="03fd6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="03fd6-102">SYNOPSIS</span></span>
<span data-ttu-id="03fd6-103">Entfernt einen autorisierungsserver.</span><span class="sxs-lookup"><span data-stu-id="03fd6-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03fd6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="03fd6-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03fd6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03fd6-105">DESCRIPTION</span></span>
<span data-ttu-id="03fd6-106">Das Cmdlet **Remove-AzureRmApiManagementAuthorizationServer** entfernt einen Azure API-Verwaltungs autorisierungsserver.</span><span class="sxs-lookup"><span data-stu-id="03fd6-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="03fd6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="03fd6-107">EXAMPLES</span></span>

## <span data-ttu-id="03fd6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="03fd6-108">PARAMETERS</span></span>

### <span data-ttu-id="03fd6-109">-Context</span><span class="sxs-lookup"><span data-stu-id="03fd6-109">-Context</span></span>
<span data-ttu-id="03fd6-110">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="03fd6-110">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="03fd6-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03fd6-111">-PassThru</span></span>
<span data-ttu-id="03fd6-112">passthru</span><span class="sxs-lookup"><span data-stu-id="03fd6-112">passthru</span></span>

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

### <span data-ttu-id="03fd6-113">-Server-Nr</span><span class="sxs-lookup"><span data-stu-id="03fd6-113">-ServerId</span></span>
<span data-ttu-id="03fd6-114">Gibt die ID des zu entfernenden autorisierungsservers an.</span><span class="sxs-lookup"><span data-stu-id="03fd6-114">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="03fd6-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="03fd6-115">-Confirm</span></span>
<span data-ttu-id="03fd6-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="03fd6-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03fd6-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03fd6-117">-WhatIf</span></span>
<span data-ttu-id="03fd6-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="03fd6-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03fd6-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="03fd6-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03fd6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03fd6-120">-DefaultProfile</span></span>
<span data-ttu-id="03fd6-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="03fd6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03fd6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03fd6-122">CommonParameters</span></span>
<span data-ttu-id="03fd6-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03fd6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03fd6-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03fd6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03fd6-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="03fd6-125">INPUTS</span></span>

## <span data-ttu-id="03fd6-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="03fd6-126">OUTPUTS</span></span>

### <span data-ttu-id="03fd6-127">Boolean</span><span class="sxs-lookup"><span data-stu-id="03fd6-127">Boolean</span></span>

## <span data-ttu-id="03fd6-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="03fd6-128">NOTES</span></span>

## <span data-ttu-id="03fd6-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="03fd6-129">RELATED LINKS</span></span>

[<span data-ttu-id="03fd6-130">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="03fd6-130">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="03fd6-131">Neu – AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="03fd6-131">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="03fd6-132">Satz-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="03fd6-132">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


