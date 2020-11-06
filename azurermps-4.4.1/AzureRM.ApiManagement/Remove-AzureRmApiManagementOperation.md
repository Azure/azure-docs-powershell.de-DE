---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: 685da9955f272066ec39890ea0f3a063d3b2f9b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479398"
---
# <span data-ttu-id="de5d4-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="de5d4-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="de5d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="de5d4-102">SYNOPSIS</span></span>
<span data-ttu-id="de5d4-103">Entfernt einen vorhandenen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="de5d4-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de5d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="de5d4-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de5d4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de5d4-105">DESCRIPTION</span></span>
<span data-ttu-id="de5d4-106">Das Cmdlet **Remove-AzureRmApiManagementOperation** entfernt einen vorhandenen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="de5d4-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="de5d4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de5d4-107">EXAMPLES</span></span>

### <span data-ttu-id="de5d4-108">Beispiel 1: Entfernen eines vorhandenen API-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="de5d4-108">Example 1: Remove an existing API Operation</span></span>
```
PS C:\>Remove-AzureRmApiManagementOperation -Context $APImContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="de5d4-109">Mit diesem Befehl wird ein vorhandener API-Vorgang entfernt.</span><span class="sxs-lookup"><span data-stu-id="de5d4-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="de5d4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="de5d4-110">PARAMETERS</span></span>

### <span data-ttu-id="de5d4-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="de5d4-111">-ApiId</span></span>
<span data-ttu-id="de5d4-112">Gibt den Bezeichner der API an.</span><span class="sxs-lookup"><span data-stu-id="de5d4-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="de5d4-113">-Context</span><span class="sxs-lookup"><span data-stu-id="de5d4-113">-Context</span></span>
<span data-ttu-id="de5d4-114">Gibt eine Instanz von **PsApiManagementContext** an.</span><span class="sxs-lookup"><span data-stu-id="de5d4-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="de5d4-115">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="de5d4-115">-OperationId</span></span>
<span data-ttu-id="de5d4-116">Gibt den Bezeichner des API-Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="de5d4-116">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="de5d4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de5d4-117">-PassThru</span></span>
<span data-ttu-id="de5d4-118">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn es erfolgreich ist, oder einen Wert von $false, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="de5d4-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="de5d4-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="de5d4-119">-Confirm</span></span>
<span data-ttu-id="de5d4-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="de5d4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de5d4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de5d4-121">-WhatIf</span></span>
<span data-ttu-id="de5d4-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="de5d4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de5d4-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="de5d4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de5d4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de5d4-124">-DefaultProfile</span></span>
<span data-ttu-id="de5d4-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="de5d4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de5d4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de5d4-126">CommonParameters</span></span>
<span data-ttu-id="de5d4-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de5d4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de5d4-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de5d4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de5d4-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="de5d4-129">INPUTS</span></span>

## <span data-ttu-id="de5d4-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="de5d4-130">OUTPUTS</span></span>

### <span data-ttu-id="de5d4-131">bool</span><span class="sxs-lookup"><span data-stu-id="de5d4-131">bool</span></span>

## <span data-ttu-id="de5d4-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="de5d4-132">NOTES</span></span>

## <span data-ttu-id="de5d4-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="de5d4-133">RELATED LINKS</span></span>

[<span data-ttu-id="de5d4-134">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="de5d4-134">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="de5d4-135">Neu – AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="de5d4-135">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="de5d4-136">Satz-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="de5d4-136">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


