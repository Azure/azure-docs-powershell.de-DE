---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: c9133c7a2924b4151afd01f257fe6b54a9eeb00d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504630"
---
# <span data-ttu-id="af639-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="af639-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="af639-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="af639-102">SYNOPSIS</span></span>
<span data-ttu-id="af639-103">Entfernt einen autorisierungsserver.</span><span class="sxs-lookup"><span data-stu-id="af639-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af639-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="af639-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af639-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="af639-105">DESCRIPTION</span></span>
<span data-ttu-id="af639-106">Das Cmdlet **Remove-AzureRmApiManagementAuthorizationServer** entfernt einen Azure API-Verwaltungs autorisierungsserver.</span><span class="sxs-lookup"><span data-stu-id="af639-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="af639-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="af639-107">EXAMPLES</span></span>

## <span data-ttu-id="af639-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="af639-108">PARAMETERS</span></span>

### <span data-ttu-id="af639-109">-Context</span><span class="sxs-lookup"><span data-stu-id="af639-109">-Context</span></span>
<span data-ttu-id="af639-110">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="af639-110">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="af639-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af639-111">-DefaultProfile</span></span>
<span data-ttu-id="af639-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="af639-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="af639-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af639-113">-PassThru</span></span>
<span data-ttu-id="af639-114">passthru</span><span class="sxs-lookup"><span data-stu-id="af639-114">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af639-115">-Server-Nr</span><span class="sxs-lookup"><span data-stu-id="af639-115">-ServerId</span></span>
<span data-ttu-id="af639-116">Gibt die ID des zu entfernenden autorisierungsservers an.</span><span class="sxs-lookup"><span data-stu-id="af639-116">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="af639-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="af639-117">-Confirm</span></span>
<span data-ttu-id="af639-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="af639-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af639-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af639-119">-WhatIf</span></span>
<span data-ttu-id="af639-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af639-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af639-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="af639-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af639-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af639-122">CommonParameters</span></span>
<span data-ttu-id="af639-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af639-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af639-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af639-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af639-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="af639-125">INPUTS</span></span>

### <span data-ttu-id="af639-126">Keine</span><span class="sxs-lookup"><span data-stu-id="af639-126">None</span></span>
<span data-ttu-id="af639-127">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="af639-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="af639-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="af639-128">OUTPUTS</span></span>

### <span data-ttu-id="af639-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="af639-129">Boolean</span></span>

## <span data-ttu-id="af639-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="af639-130">NOTES</span></span>

## <span data-ttu-id="af639-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="af639-131">RELATED LINKS</span></span>

[<span data-ttu-id="af639-132">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="af639-132">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="af639-133">Neu – AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="af639-133">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="af639-134">Satz-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="af639-134">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


