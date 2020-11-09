---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 073b32936be1e1614e495ca680a250498742ba66
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300892"
---
# <span data-ttu-id="966bc-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="966bc-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="966bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="966bc-102">SYNOPSIS</span></span>
<span data-ttu-id="966bc-103">Entfernt ein Back-End.</span><span class="sxs-lookup"><span data-stu-id="966bc-103">Removes a Backend.</span></span>

## <span data-ttu-id="966bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="966bc-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="966bc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="966bc-105">DESCRIPTION</span></span>
<span data-ttu-id="966bc-106">Entfernt ein vom Bezeichner angegebenes Back-End aus der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="966bc-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="966bc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="966bc-107">EXAMPLES</span></span>

### <span data-ttu-id="966bc-108">Beispiel 1: Entfernen des Back-End-123</span><span class="sxs-lookup"><span data-stu-id="966bc-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="966bc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="966bc-109">PARAMETERS</span></span>

### <span data-ttu-id="966bc-110">-Back-End-Nr</span><span class="sxs-lookup"><span data-stu-id="966bc-110">-BackendId</span></span>
<span data-ttu-id="966bc-111">Bezeichner des vorhandenen Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="966bc-111">Identifier of existing backend.</span></span>
<span data-ttu-id="966bc-112">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="966bc-112">This parameter is required.</span></span>

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

### <span data-ttu-id="966bc-113">-Context</span><span class="sxs-lookup"><span data-stu-id="966bc-113">-Context</span></span>
<span data-ttu-id="966bc-114">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="966bc-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="966bc-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="966bc-115">This parameter is required.</span></span>

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

### <span data-ttu-id="966bc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="966bc-116">-DefaultProfile</span></span>
<span data-ttu-id="966bc-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="966bc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="966bc-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="966bc-118">-PassThru</span></span>
<span data-ttu-id="966bc-119">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="966bc-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="966bc-120">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="966bc-120">This parameter is optional.</span></span>
<span data-ttu-id="966bc-121">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="966bc-121">Default value is false.</span></span>

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

### <span data-ttu-id="966bc-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="966bc-122">-Confirm</span></span>
<span data-ttu-id="966bc-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="966bc-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="966bc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="966bc-124">-WhatIf</span></span>
<span data-ttu-id="966bc-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="966bc-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="966bc-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="966bc-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="966bc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="966bc-127">CommonParameters</span></span>
<span data-ttu-id="966bc-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="966bc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="966bc-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="966bc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="966bc-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="966bc-130">INPUTS</span></span>

### <span data-ttu-id="966bc-131">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="966bc-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="966bc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="966bc-132">System.String</span></span>

### <span data-ttu-id="966bc-133">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="966bc-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="966bc-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="966bc-134">OUTPUTS</span></span>

### <span data-ttu-id="966bc-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="966bc-135">System.Boolean</span></span>

## <span data-ttu-id="966bc-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="966bc-136">NOTES</span></span>

## <span data-ttu-id="966bc-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="966bc-137">RELATED LINKS</span></span>

[<span data-ttu-id="966bc-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="966bc-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="966bc-139">Neu – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="966bc-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="966bc-140">Neu – AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="966bc-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="966bc-141">Neu – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="966bc-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="966bc-142">Satz-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="966bc-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
