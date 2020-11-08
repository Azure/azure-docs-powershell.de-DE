---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 74e876621948587c116f435f70315c04b403c2f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005281"
---
# <span data-ttu-id="3c9ce-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="3c9ce-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="3c9ce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3c9ce-102">SYNOPSIS</span></span>
<span data-ttu-id="3c9ce-103">Entfernt einen autorisierungsserver.</span><span class="sxs-lookup"><span data-stu-id="3c9ce-103">Removes an authorization server.</span></span>

## <span data-ttu-id="3c9ce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c9ce-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c9ce-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c9ce-105">DESCRIPTION</span></span>
<span data-ttu-id="3c9ce-106">Das Cmdlet **Remove-AzApiManagementAuthorizationServer** entfernt einen Azure API-Verwaltungs autorisierungsserver.</span><span class="sxs-lookup"><span data-stu-id="3c9ce-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="3c9ce-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3c9ce-107">EXAMPLES</span></span>

### <span data-ttu-id="3c9ce-108">Beispiel 1: Entfernen eines autorisierungsservers</span><span class="sxs-lookup"><span data-stu-id="3c9ce-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="3c9ce-109">Mit diesem Befehl wird der angegebene API-Verwaltungs Autorisierungs Server entfernt.</span><span class="sxs-lookup"><span data-stu-id="3c9ce-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="3c9ce-110">Da der Parameter *Force* angegeben ist, ist keine Bestätigung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3c9ce-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="3c9ce-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c9ce-111">PARAMETERS</span></span>

### <span data-ttu-id="3c9ce-112">-Context</span><span class="sxs-lookup"><span data-stu-id="3c9ce-112">-Context</span></span>
<span data-ttu-id="3c9ce-113">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3c9ce-113">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3c9ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c9ce-114">-DefaultProfile</span></span>
<span data-ttu-id="3c9ce-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3c9ce-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c9ce-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c9ce-116">-PassThru</span></span>
<span data-ttu-id="3c9ce-117">passthru</span><span class="sxs-lookup"><span data-stu-id="3c9ce-117">passthru</span></span>

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

### <span data-ttu-id="3c9ce-118">-Server-Nr</span><span class="sxs-lookup"><span data-stu-id="3c9ce-118">-ServerId</span></span>
<span data-ttu-id="3c9ce-119">Gibt die ID des zu entfernenden autorisierungsservers an.</span><span class="sxs-lookup"><span data-stu-id="3c9ce-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="3c9ce-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3c9ce-120">-Confirm</span></span>
<span data-ttu-id="3c9ce-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3c9ce-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c9ce-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c9ce-122">-WhatIf</span></span>
<span data-ttu-id="3c9ce-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c9ce-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c9ce-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3c9ce-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c9ce-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c9ce-125">CommonParameters</span></span>
<span data-ttu-id="3c9ce-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c9ce-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c9ce-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c9ce-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c9ce-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3c9ce-128">INPUTS</span></span>

### <span data-ttu-id="3c9ce-129">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3c9ce-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3c9ce-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3c9ce-130">System.String</span></span>

### <span data-ttu-id="3c9ce-131">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="3c9ce-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3c9ce-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3c9ce-132">OUTPUTS</span></span>

### <span data-ttu-id="3c9ce-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c9ce-133">System.Boolean</span></span>

## <span data-ttu-id="3c9ce-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="3c9ce-134">NOTES</span></span>

## <span data-ttu-id="3c9ce-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3c9ce-135">RELATED LINKS</span></span>

[<span data-ttu-id="3c9ce-136">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="3c9ce-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="3c9ce-137">Neu – AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="3c9ce-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="3c9ce-138">Satz-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="3c9ce-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


