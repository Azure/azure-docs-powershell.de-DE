---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
ms.openlocfilehash: fd232a0f118db5730c41ef1588eaf07d80df69f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477406"
---
# <span data-ttu-id="d7d3d-101">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d7d3d-101">Remove-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="d7d3d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="d7d3d-103">Löscht ein vorhandenes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-103">Deletes an existing subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7d3d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7d3d-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7d3d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7d3d-105">DESCRIPTION</span></span>
<span data-ttu-id="d7d3d-106">Das Cmdlet **Remove-AzureRmApiManagementSubscription** löscht ein vorhandenes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-106">The **Remove-AzureRmApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="d7d3d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7d3d-107">EXAMPLES</span></span>

### <span data-ttu-id="d7d3d-108">Beispiel 1: Löschen eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="d7d3d-108">Example 1: Delete a subscription</span></span>
```
PS C:\>Remove-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="d7d3d-109">Mit diesem Befehl wird ein vorhandenes Abonnement gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="d7d3d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7d3d-110">PARAMETERS</span></span>

### <span data-ttu-id="d7d3d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d7d3d-111">-Context</span></span>
<span data-ttu-id="d7d3d-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d7d3d-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7d3d-113">-PassThru</span></span>
<span data-ttu-id="d7d3d-114">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn dies erfolgreich ist, oder einen Wert von $false, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-114">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="d7d3d-115">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="d7d3d-115">-SubscriptionId</span></span>
<span data-ttu-id="d7d3d-116">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-116">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="d7d3d-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d7d3d-117">-Confirm</span></span>
<span data-ttu-id="d7d3d-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7d3d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7d3d-119">-WhatIf</span></span>
<span data-ttu-id="d7d3d-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7d3d-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7d3d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7d3d-122">-DefaultProfile</span></span>
<span data-ttu-id="d7d3d-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7d3d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7d3d-124">CommonParameters</span></span>
<span data-ttu-id="d7d3d-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7d3d-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7d3d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7d3d-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7d3d-127">INPUTS</span></span>

## <span data-ttu-id="d7d3d-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7d3d-128">OUTPUTS</span></span>

### <span data-ttu-id="d7d3d-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="d7d3d-129">Boolean</span></span>

## <span data-ttu-id="d7d3d-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7d3d-130">NOTES</span></span>

## <span data-ttu-id="d7d3d-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7d3d-131">RELATED LINKS</span></span>

[<span data-ttu-id="d7d3d-132">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d7d3d-132">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="d7d3d-133">Neu – AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d7d3d-133">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="d7d3d-134">Satz-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d7d3d-134">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


