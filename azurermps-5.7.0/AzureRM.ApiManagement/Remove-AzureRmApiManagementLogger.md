---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
ms.openlocfilehash: 2dbd515877e44023077d782080cff29d78a0e6fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504626"
---
# <span data-ttu-id="684cf-101">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="684cf-101">Remove-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="684cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="684cf-102">SYNOPSIS</span></span>
<span data-ttu-id="684cf-103">Entfernt eine API-verwaltungsprotokollierung.</span><span class="sxs-lookup"><span data-stu-id="684cf-103">Removes an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="684cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="684cf-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="684cf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="684cf-105">DESCRIPTION</span></span>
<span data-ttu-id="684cf-106">Das Cmdlet **Remove-AzureRmApiManagementLogger** entfernt eine Azure API-Verwaltungs **Protokollierung**.</span><span class="sxs-lookup"><span data-stu-id="684cf-106">The **Remove-AzureRmApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="684cf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="684cf-107">EXAMPLES</span></span>

### <span data-ttu-id="684cf-108">Beispiel 1: Entfernen einer Protokollierung</span><span class="sxs-lookup"><span data-stu-id="684cf-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="684cf-109">Dieser Befehl entfernt eine Protokollierung mit der ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="684cf-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="684cf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="684cf-110">PARAMETERS</span></span>

### <span data-ttu-id="684cf-111">-Context</span><span class="sxs-lookup"><span data-stu-id="684cf-111">-Context</span></span>
<span data-ttu-id="684cf-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="684cf-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="684cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="684cf-113">-DefaultProfile</span></span>
<span data-ttu-id="684cf-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="684cf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="684cf-115">-Protokollierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="684cf-115">-LoggerId</span></span>
<span data-ttu-id="684cf-116">Gibt die ID der zu entfernenden Protokollierung an.</span><span class="sxs-lookup"><span data-stu-id="684cf-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="684cf-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="684cf-117">-PassThru</span></span>
<span data-ttu-id="684cf-118">Gibt an, dass dieses Cmdlet den Wert $true zurückgibt, wenn der Vorgang erfolgreich ausgeführt wird oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="684cf-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="684cf-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="684cf-119">-Confirm</span></span>
<span data-ttu-id="684cf-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="684cf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="684cf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="684cf-121">-WhatIf</span></span>
<span data-ttu-id="684cf-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="684cf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="684cf-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="684cf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="684cf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="684cf-124">CommonParameters</span></span>
<span data-ttu-id="684cf-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="684cf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="684cf-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="684cf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="684cf-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="684cf-127">INPUTS</span></span>

### <span data-ttu-id="684cf-128">Keine</span><span class="sxs-lookup"><span data-stu-id="684cf-128">None</span></span>
<span data-ttu-id="684cf-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="684cf-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="684cf-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="684cf-130">OUTPUTS</span></span>

### <span data-ttu-id="684cf-131">Boolean</span><span class="sxs-lookup"><span data-stu-id="684cf-131">Boolean</span></span>

## <span data-ttu-id="684cf-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="684cf-132">NOTES</span></span>

## <span data-ttu-id="684cf-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="684cf-133">RELATED LINKS</span></span>

[<span data-ttu-id="684cf-134">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="684cf-134">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="684cf-135">Neu – AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="684cf-135">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="684cf-136">Satz-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="684cf-136">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


