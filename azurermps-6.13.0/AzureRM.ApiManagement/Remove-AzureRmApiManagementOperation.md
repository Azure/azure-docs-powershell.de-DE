---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: 1a3fd2ca25099be029616e048c5ebfa0e398229e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476345"
---
# <span data-ttu-id="d3711-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d3711-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="d3711-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d3711-102">SYNOPSIS</span></span>
<span data-ttu-id="d3711-103">Entfernt einen vorhandenen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d3711-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3711-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3711-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3711-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3711-105">DESCRIPTION</span></span>
<span data-ttu-id="d3711-106">Das Cmdlet **Remove-AzureRmApiManagementOperation** entfernt einen vorhandenen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d3711-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="d3711-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3711-107">EXAMPLES</span></span>

### <span data-ttu-id="d3711-108">Beispiel 1: Entfernen eines vorhandenen API-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="d3711-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="d3711-109">Mit diesem Befehl wird ein vorhandener API-Vorgang entfernt.</span><span class="sxs-lookup"><span data-stu-id="d3711-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="d3711-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3711-110">PARAMETERS</span></span>

### <span data-ttu-id="d3711-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d3711-111">-ApiId</span></span>
<span data-ttu-id="d3711-112">Gibt den Bezeichner der API an.</span><span class="sxs-lookup"><span data-stu-id="d3711-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="d3711-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="d3711-113">-ApiRevision</span></span>
<span data-ttu-id="d3711-114">Bezeichner der API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="d3711-114">Identifier of API Revision.</span></span> <span data-ttu-id="d3711-115">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d3711-115">This parameter is optional.</span></span> <span data-ttu-id="d3711-116">Wenn Sie nicht angegeben wird, wird der Vorgang aus der aktuell aktiven API-Revision entfernt.</span><span class="sxs-lookup"><span data-stu-id="d3711-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3711-117">-Context</span><span class="sxs-lookup"><span data-stu-id="d3711-117">-Context</span></span>
<span data-ttu-id="d3711-118">Gibt eine Instanz von **PsApiManagementContext** an.</span><span class="sxs-lookup"><span data-stu-id="d3711-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="d3711-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3711-119">-DefaultProfile</span></span>
<span data-ttu-id="d3711-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d3711-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3711-121">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="d3711-121">-OperationId</span></span>
<span data-ttu-id="d3711-122">Gibt den Bezeichner des API-Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="d3711-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="d3711-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3711-123">-PassThru</span></span>
<span data-ttu-id="d3711-124">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn es erfolgreich ist, oder einen Wert von $false, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="d3711-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="d3711-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d3711-125">-Confirm</span></span>
<span data-ttu-id="d3711-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d3711-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3711-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3711-127">-WhatIf</span></span>
<span data-ttu-id="d3711-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3711-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3711-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3711-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3711-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3711-130">CommonParameters</span></span>
<span data-ttu-id="d3711-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3711-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3711-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3711-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3711-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d3711-133">INPUTS</span></span>

### <span data-ttu-id="d3711-134">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d3711-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d3711-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d3711-135">System.String</span></span>

### <span data-ttu-id="d3711-136">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="d3711-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d3711-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d3711-137">OUTPUTS</span></span>

### <span data-ttu-id="d3711-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d3711-138">System.Boolean</span></span>

## <span data-ttu-id="d3711-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="d3711-139">NOTES</span></span>

## <span data-ttu-id="d3711-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d3711-140">RELATED LINKS</span></span>

[<span data-ttu-id="d3711-141">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d3711-141">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="d3711-142">Neu – AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d3711-142">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="d3711-143">Satz-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d3711-143">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


