---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: 13f5297efc19aa56cc5af55962c072f5ff2a32d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996899"
---
# <span data-ttu-id="6c9c6-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6c9c6-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="6c9c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c9c6-102">SYNOPSIS</span></span>
<span data-ttu-id="6c9c6-103">Entfernt eine API.</span><span class="sxs-lookup"><span data-stu-id="6c9c6-103">Removes an API.</span></span>

## <span data-ttu-id="6c9c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c9c6-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c9c6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c9c6-105">DESCRIPTION</span></span>
<span data-ttu-id="6c9c6-106">Das Cmdlet **Remove-AzApiManagementApi** entfernt eine vorhandene API.</span><span class="sxs-lookup"><span data-stu-id="6c9c6-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="6c9c6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c9c6-107">EXAMPLES</span></span>

### <span data-ttu-id="6c9c6-108">Beispiel 1: Entfernen einer API</span><span class="sxs-lookup"><span data-stu-id="6c9c6-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="6c9c6-109">Mit diesem Befehl wird die API mit der angegebenen ID entfernt.</span><span class="sxs-lookup"><span data-stu-id="6c9c6-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="6c9c6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c9c6-110">PARAMETERS</span></span>

### <span data-ttu-id="6c9c6-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6c9c6-111">-ApiId</span></span>
<span data-ttu-id="6c9c6-112">Gibt die ID der API-Entfernung an.</span><span class="sxs-lookup"><span data-stu-id="6c9c6-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="6c9c6-113">-Context</span><span class="sxs-lookup"><span data-stu-id="6c9c6-113">-Context</span></span>
<span data-ttu-id="6c9c6-114">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="6c9c6-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c9c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c9c6-115">-DefaultProfile</span></span>
<span data-ttu-id="6c9c6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6c9c6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c9c6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c9c6-117">-PassThru</span></span>
<span data-ttu-id="6c9c6-118">passthru</span><span class="sxs-lookup"><span data-stu-id="6c9c6-118">passthru</span></span>

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

### <span data-ttu-id="6c9c6-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6c9c6-119">-Confirm</span></span>
<span data-ttu-id="6c9c6-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6c9c6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c9c6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c9c6-121">-WhatIf</span></span>
<span data-ttu-id="6c9c6-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6c9c6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c9c6-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c9c6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c9c6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c9c6-124">CommonParameters</span></span>
<span data-ttu-id="6c9c6-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c9c6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c9c6-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c9c6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c9c6-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c9c6-127">INPUTS</span></span>

### <span data-ttu-id="6c9c6-128">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6c9c6-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6c9c6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6c9c6-129">System.String</span></span>

### <span data-ttu-id="6c9c6-130">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="6c9c6-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6c9c6-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c9c6-131">OUTPUTS</span></span>

### <span data-ttu-id="6c9c6-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6c9c6-132">System.Boolean</span></span>

## <span data-ttu-id="6c9c6-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c9c6-133">NOTES</span></span>

## <span data-ttu-id="6c9c6-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c9c6-134">RELATED LINKS</span></span>

[<span data-ttu-id="6c9c6-135">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6c9c6-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="6c9c6-136">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6c9c6-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="6c9c6-137">Importieren-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6c9c6-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="6c9c6-138">Neu – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6c9c6-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="6c9c6-139">Satz-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6c9c6-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


