---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
ms.openlocfilehash: cadae96af05ae11f76d3a8ea0010da4d73161186
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477442"
---
# <span data-ttu-id="93852-101">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="93852-101">Remove-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="93852-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93852-102">SYNOPSIS</span></span>
<span data-ttu-id="93852-103">Entfernt eine API.</span><span class="sxs-lookup"><span data-stu-id="93852-103">Removes an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93852-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93852-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93852-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93852-105">DESCRIPTION</span></span>
<span data-ttu-id="93852-106">Das Cmdlet **Remove-AzureRmApiManagementApi** entfernt eine vorhandene API.</span><span class="sxs-lookup"><span data-stu-id="93852-106">The **Remove-AzureRmApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="93852-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93852-107">EXAMPLES</span></span>

### <span data-ttu-id="93852-108">Beispiel 1: Entfernen einer API</span><span class="sxs-lookup"><span data-stu-id="93852-108">Example 1: Remove an API</span></span>
```
PS C:\>Remove-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789"
```

<span data-ttu-id="93852-109">Mit diesem Befehl wird die API mit der angegebenen ID entfernt.</span><span class="sxs-lookup"><span data-stu-id="93852-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="93852-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="93852-110">PARAMETERS</span></span>

### <span data-ttu-id="93852-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="93852-111">-ApiId</span></span>
<span data-ttu-id="93852-112">Gibt die ID der API-Entfernung an.</span><span class="sxs-lookup"><span data-stu-id="93852-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="93852-113">-Context</span><span class="sxs-lookup"><span data-stu-id="93852-113">-Context</span></span>
<span data-ttu-id="93852-114">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="93852-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="93852-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93852-115">-PassThru</span></span>
<span data-ttu-id="93852-116">passthru</span><span class="sxs-lookup"><span data-stu-id="93852-116">passthru</span></span>

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

### <span data-ttu-id="93852-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="93852-117">-Confirm</span></span>
<span data-ttu-id="93852-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="93852-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93852-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93852-119">-WhatIf</span></span>
<span data-ttu-id="93852-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="93852-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93852-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="93852-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93852-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93852-122">-DefaultProfile</span></span>
<span data-ttu-id="93852-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="93852-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93852-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93852-124">CommonParameters</span></span>
<span data-ttu-id="93852-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93852-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93852-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93852-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93852-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93852-127">INPUTS</span></span>

## <span data-ttu-id="93852-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93852-128">OUTPUTS</span></span>

### <span data-ttu-id="93852-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="93852-129">Boolean</span></span>

## <span data-ttu-id="93852-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="93852-130">NOTES</span></span>

## <span data-ttu-id="93852-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93852-131">RELATED LINKS</span></span>

[<span data-ttu-id="93852-132">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="93852-132">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="93852-133">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="93852-133">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="93852-134">Importieren-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="93852-134">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="93852-135">Neu – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="93852-135">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="93852-136">Satz-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="93852-136">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


