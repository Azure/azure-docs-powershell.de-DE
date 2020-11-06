---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
ms.openlocfilehash: cf27d54e50d320d0ad20a3e847cf2b9dda8ac3c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500301"
---
# <span data-ttu-id="93fca-101">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="93fca-101">Remove-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="93fca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93fca-102">SYNOPSIS</span></span>
<span data-ttu-id="93fca-103">Entfernt eine API.</span><span class="sxs-lookup"><span data-stu-id="93fca-103">Removes an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93fca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93fca-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93fca-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93fca-105">DESCRIPTION</span></span>
<span data-ttu-id="93fca-106">Das Cmdlet **Remove-AzureRmApiManagementApi** entfernt eine vorhandene API.</span><span class="sxs-lookup"><span data-stu-id="93fca-106">The **Remove-AzureRmApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="93fca-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93fca-107">EXAMPLES</span></span>

### <span data-ttu-id="93fca-108">Beispiel 1: Entfernen einer API</span><span class="sxs-lookup"><span data-stu-id="93fca-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="93fca-109">Mit diesem Befehl wird die API mit der angegebenen ID entfernt.</span><span class="sxs-lookup"><span data-stu-id="93fca-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="93fca-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="93fca-110">PARAMETERS</span></span>

### <span data-ttu-id="93fca-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="93fca-111">-ApiId</span></span>
<span data-ttu-id="93fca-112">Gibt die ID der API-Entfernung an.</span><span class="sxs-lookup"><span data-stu-id="93fca-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="93fca-113">-Context</span><span class="sxs-lookup"><span data-stu-id="93fca-113">-Context</span></span>
<span data-ttu-id="93fca-114">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="93fca-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="93fca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93fca-115">-DefaultProfile</span></span>
<span data-ttu-id="93fca-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="93fca-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93fca-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93fca-117">-PassThru</span></span>
<span data-ttu-id="93fca-118">passthru</span><span class="sxs-lookup"><span data-stu-id="93fca-118">passthru</span></span>

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

### <span data-ttu-id="93fca-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="93fca-119">-Confirm</span></span>
<span data-ttu-id="93fca-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="93fca-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93fca-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93fca-121">-WhatIf</span></span>
<span data-ttu-id="93fca-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="93fca-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93fca-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="93fca-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93fca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93fca-124">CommonParameters</span></span>
<span data-ttu-id="93fca-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93fca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93fca-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93fca-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93fca-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93fca-127">INPUTS</span></span>

### <span data-ttu-id="93fca-128">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="93fca-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="93fca-129">System. String</span><span class="sxs-lookup"><span data-stu-id="93fca-129">System.String</span></span>

### <span data-ttu-id="93fca-130">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="93fca-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="93fca-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93fca-131">OUTPUTS</span></span>

### <span data-ttu-id="93fca-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="93fca-132">System.Boolean</span></span>

## <span data-ttu-id="93fca-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="93fca-133">NOTES</span></span>

## <span data-ttu-id="93fca-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93fca-134">RELATED LINKS</span></span>

[<span data-ttu-id="93fca-135">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="93fca-135">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="93fca-136">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="93fca-136">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="93fca-137">Importieren-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="93fca-137">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="93fca-138">Neu – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="93fca-138">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="93fca-139">Satz-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="93fca-139">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


