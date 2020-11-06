---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: ef3db99522c07b593493e30bd3778f1774af1a5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503133"
---
# <span data-ttu-id="02525-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="02525-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="02525-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="02525-102">SYNOPSIS</span></span>
<span data-ttu-id="02525-103">Entfernt einen vorhandenen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="02525-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02525-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="02525-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02525-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02525-105">DESCRIPTION</span></span>
<span data-ttu-id="02525-106">Das Cmdlet **Remove-AzureRmApiManagementOperation** entfernt einen vorhandenen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="02525-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="02525-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02525-107">EXAMPLES</span></span>

### <span data-ttu-id="02525-108">Beispiel 1: Entfernen eines vorhandenen API-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="02525-108">Example 1: Remove an existing API Operation</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="02525-109">Mit diesem Befehl wird ein vorhandener API-Vorgang entfernt.</span><span class="sxs-lookup"><span data-stu-id="02525-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="02525-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="02525-110">PARAMETERS</span></span>

### <span data-ttu-id="02525-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="02525-111">-ApiId</span></span>
<span data-ttu-id="02525-112">Gibt den Bezeichner der API an.</span><span class="sxs-lookup"><span data-stu-id="02525-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="02525-113">-Context</span><span class="sxs-lookup"><span data-stu-id="02525-113">-Context</span></span>
<span data-ttu-id="02525-114">Gibt eine Instanz von **PsApiManagementContext** an.</span><span class="sxs-lookup"><span data-stu-id="02525-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="02525-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02525-115">-DefaultProfile</span></span>
<span data-ttu-id="02525-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="02525-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="02525-117">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="02525-117">-OperationId</span></span>
<span data-ttu-id="02525-118">Gibt den Bezeichner des API-Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="02525-118">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="02525-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02525-119">-PassThru</span></span>
<span data-ttu-id="02525-120">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn es erfolgreich ist, oder einen Wert von $false, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="02525-120">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="02525-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="02525-121">-Confirm</span></span>
<span data-ttu-id="02525-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="02525-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02525-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02525-123">-WhatIf</span></span>
<span data-ttu-id="02525-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02525-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02525-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="02525-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02525-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02525-126">CommonParameters</span></span>
<span data-ttu-id="02525-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02525-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02525-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02525-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02525-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="02525-129">INPUTS</span></span>

### <span data-ttu-id="02525-130">Keine</span><span class="sxs-lookup"><span data-stu-id="02525-130">None</span></span>
<span data-ttu-id="02525-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="02525-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="02525-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="02525-132">OUTPUTS</span></span>

### <span data-ttu-id="02525-133">bool</span><span class="sxs-lookup"><span data-stu-id="02525-133">bool</span></span>

## <span data-ttu-id="02525-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="02525-134">NOTES</span></span>

## <span data-ttu-id="02525-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="02525-135">RELATED LINKS</span></span>

[<span data-ttu-id="02525-136">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="02525-136">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="02525-137">Neu – AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="02525-137">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="02525-138">Satz-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="02525-138">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


