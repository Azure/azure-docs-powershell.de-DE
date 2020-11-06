---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
ms.openlocfilehash: 6be4c714627d77b0e3c56b8dd9766c550deebd7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477401"
---
# <span data-ttu-id="b2299-101">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b2299-101">Remove-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="b2299-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2299-102">SYNOPSIS</span></span>
<span data-ttu-id="b2299-103">Löscht einen vorhandenen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b2299-103">Deletes an existing user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2299-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2299-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2299-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2299-105">DESCRIPTION</span></span>
<span data-ttu-id="b2299-106">Das Cmdlet **Remove-AzureRmApiManagementUser** löscht einen vorhandenen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b2299-106">The **Remove-AzureRmApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="b2299-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2299-107">EXAMPLES</span></span>

### <span data-ttu-id="b2299-108">Beispiel 1: Löschen eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="b2299-108">Example 1: Delete a user</span></span>
```
PS C:\>Remove-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="b2299-109">Dieser Befehl löscht einen vorhandenen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b2299-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="b2299-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2299-110">PARAMETERS</span></span>

### <span data-ttu-id="b2299-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b2299-111">-Context</span></span>
<span data-ttu-id="b2299-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b2299-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="b2299-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b2299-113">This parameter is required.</span></span>

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

### <span data-ttu-id="b2299-114">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="b2299-114">-DeleteSubscriptions</span></span>
<span data-ttu-id="b2299-115">Gibt an, ob Abonnements für das Produkt gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b2299-115">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="b2299-116">Wenn dieser Parameter nicht angegeben ist und ein Abonnement vorhanden ist, löst dieses Cmdlet eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="b2299-116">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="b2299-117">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="b2299-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="b2299-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2299-118">-PassThru</span></span>
<span data-ttu-id="b2299-119">Gibt an, dass dieses Cmdlet einen Wert von $Ture zurückgibt, wenn dies erfolgreich ist, oder einen Wert von $false, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="b2299-119">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="b2299-120">-UserID</span><span class="sxs-lookup"><span data-stu-id="b2299-120">-UserId</span></span>
<span data-ttu-id="b2299-121">Gibt die ID des Benutzers an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2299-121">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="b2299-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b2299-122">-Confirm</span></span>
<span data-ttu-id="b2299-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2299-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2299-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2299-124">-WhatIf</span></span>
<span data-ttu-id="b2299-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2299-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2299-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2299-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2299-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2299-127">-DefaultProfile</span></span>
<span data-ttu-id="b2299-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b2299-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2299-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2299-129">CommonParameters</span></span>
<span data-ttu-id="b2299-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2299-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2299-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2299-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2299-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2299-132">INPUTS</span></span>

## <span data-ttu-id="b2299-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2299-133">OUTPUTS</span></span>

### <span data-ttu-id="b2299-134">Boolean</span><span class="sxs-lookup"><span data-stu-id="b2299-134">Boolean</span></span>

## <span data-ttu-id="b2299-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2299-135">NOTES</span></span>

## <span data-ttu-id="b2299-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2299-136">RELATED LINKS</span></span>

[<span data-ttu-id="b2299-137">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b2299-137">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="b2299-138">Neu – AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b2299-138">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="b2299-139">Satz-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b2299-139">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


