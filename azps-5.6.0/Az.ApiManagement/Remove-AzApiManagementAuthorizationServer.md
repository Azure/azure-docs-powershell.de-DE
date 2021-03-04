---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 8cbb9afc37242330bc76b7413033dc41cbd61cd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929115"
---
# <span data-ttu-id="26bf5-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="26bf5-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="26bf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="26bf5-103">Entfernt einen Autorisierungsserver.</span><span class="sxs-lookup"><span data-stu-id="26bf5-103">Removes an authorization server.</span></span>

## <span data-ttu-id="26bf5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26bf5-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26bf5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26bf5-105">DESCRIPTION</span></span>
<span data-ttu-id="26bf5-106">Das **Cmdlet Remove-AzApiManagementAuthorizationServer** entfernt einen Azure API Management-Autorisierungsserver.</span><span class="sxs-lookup"><span data-stu-id="26bf5-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="26bf5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="26bf5-107">EXAMPLES</span></span>

### <span data-ttu-id="26bf5-108">Beispiel 1: Entfernen eines Autorisierungsservers</span><span class="sxs-lookup"><span data-stu-id="26bf5-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="26bf5-109">Mit diesem Befehl wird der angegebene API-Verwaltungsautorisierungsserver entfernt.</span><span class="sxs-lookup"><span data-stu-id="26bf5-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="26bf5-110">Da der *Parameter Erzwingen* angegeben ist, ist keine Bestätigung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="26bf5-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="26bf5-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="26bf5-111">PARAMETERS</span></span>

### <span data-ttu-id="26bf5-112">-Context</span><span class="sxs-lookup"><span data-stu-id="26bf5-112">-Context</span></span>
<span data-ttu-id="26bf5-113">Gibt ein **PsApiManagementContext-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="26bf5-113">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="26bf5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26bf5-114">-DefaultProfile</span></span>
<span data-ttu-id="26bf5-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26bf5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26bf5-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26bf5-116">-PassThru</span></span>
<span data-ttu-id="26bf5-117">passthru</span><span class="sxs-lookup"><span data-stu-id="26bf5-117">passthru</span></span>

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

### <span data-ttu-id="26bf5-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="26bf5-118">-ServerId</span></span>
<span data-ttu-id="26bf5-119">Gibt die ID des zu entfernenden Autorisierungsservers an.</span><span class="sxs-lookup"><span data-stu-id="26bf5-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="26bf5-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="26bf5-120">-Confirm</span></span>
<span data-ttu-id="26bf5-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="26bf5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26bf5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26bf5-122">-WhatIf</span></span>
<span data-ttu-id="26bf5-123">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26bf5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26bf5-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26bf5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26bf5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26bf5-125">CommonParameters</span></span>
<span data-ttu-id="26bf5-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26bf5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26bf5-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26bf5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26bf5-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="26bf5-128">INPUTS</span></span>

### <span data-ttu-id="26bf5-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="26bf5-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="26bf5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="26bf5-130">System.String</span></span>

### <span data-ttu-id="26bf5-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="26bf5-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="26bf5-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="26bf5-132">OUTPUTS</span></span>

### <span data-ttu-id="26bf5-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="26bf5-133">System.Boolean</span></span>

## <span data-ttu-id="26bf5-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="26bf5-134">NOTES</span></span>

## <span data-ttu-id="26bf5-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="26bf5-135">RELATED LINKS</span></span>

[<span data-ttu-id="26bf5-136">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="26bf5-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="26bf5-137">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="26bf5-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="26bf5-138">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="26bf5-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


