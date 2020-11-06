---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
ms.openlocfilehash: 3c36d0b21b1fdda1282a1184f90728e827515195
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479997"
---
# <span data-ttu-id="89b5a-101">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="89b5a-101">Remove-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="89b5a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="89b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="89b5a-103">Entfernt eine API-verwaltungsprotokollierung.</span><span class="sxs-lookup"><span data-stu-id="89b5a-103">Removes an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89b5a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="89b5a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89b5a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89b5a-105">DESCRIPTION</span></span>
<span data-ttu-id="89b5a-106">Das Cmdlet **Remove-AzureRmApiManagementLogger** entfernt eine Azure API-Verwaltungs **Protokollierung**.</span><span class="sxs-lookup"><span data-stu-id="89b5a-106">The **Remove-AzureRmApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="89b5a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89b5a-107">EXAMPLES</span></span>

### <span data-ttu-id="89b5a-108">Beispiel 1: Entfernen einer Protokollierung</span><span class="sxs-lookup"><span data-stu-id="89b5a-108">Example 1: Remove a logger</span></span>
```
PS C:\>Remove-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="89b5a-109">Dieser Befehl entfernt eine Protokollierung mit der ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="89b5a-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="89b5a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="89b5a-110">PARAMETERS</span></span>

### <span data-ttu-id="89b5a-111">-Context</span><span class="sxs-lookup"><span data-stu-id="89b5a-111">-Context</span></span>
<span data-ttu-id="89b5a-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="89b5a-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="89b5a-113">-Protokollierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="89b5a-113">-LoggerId</span></span>
<span data-ttu-id="89b5a-114">Gibt die ID der zu entfernenden Protokollierung an.</span><span class="sxs-lookup"><span data-stu-id="89b5a-114">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="89b5a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89b5a-115">-PassThru</span></span>
<span data-ttu-id="89b5a-116">Gibt an, dass dieses Cmdlet den Wert $true zurückgibt, wenn der Vorgang erfolgreich ausgeführt wird oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="89b5a-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="89b5a-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="89b5a-117">-Confirm</span></span>
<span data-ttu-id="89b5a-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="89b5a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89b5a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89b5a-119">-WhatIf</span></span>
<span data-ttu-id="89b5a-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="89b5a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89b5a-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="89b5a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89b5a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89b5a-122">-DefaultProfile</span></span>
<span data-ttu-id="89b5a-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="89b5a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89b5a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89b5a-124">CommonParameters</span></span>
<span data-ttu-id="89b5a-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89b5a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89b5a-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89b5a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89b5a-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="89b5a-127">INPUTS</span></span>

## <span data-ttu-id="89b5a-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="89b5a-128">OUTPUTS</span></span>

### <span data-ttu-id="89b5a-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="89b5a-129">Boolean</span></span>

## <span data-ttu-id="89b5a-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="89b5a-130">NOTES</span></span>

## <span data-ttu-id="89b5a-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="89b5a-131">RELATED LINKS</span></span>

[<span data-ttu-id="89b5a-132">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="89b5a-132">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="89b5a-133">Neu – AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="89b5a-133">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="89b5a-134">Satz-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="89b5a-134">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


