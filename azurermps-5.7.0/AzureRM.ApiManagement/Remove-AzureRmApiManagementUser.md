---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
ms.openlocfilehash: 5d657610ddce1c0397a5f9e8c11b832b3fcd472b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665330"
---
# <span data-ttu-id="09c0f-101">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="09c0f-101">Remove-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="09c0f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09c0f-102">SYNOPSIS</span></span>
<span data-ttu-id="09c0f-103">Löscht einen vorhandenen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="09c0f-103">Deletes an existing user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09c0f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09c0f-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09c0f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09c0f-105">DESCRIPTION</span></span>
<span data-ttu-id="09c0f-106">Das Cmdlet **Remove-AzureRmApiManagementUser** löscht einen vorhandenen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="09c0f-106">The **Remove-AzureRmApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="09c0f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09c0f-107">EXAMPLES</span></span>

### <span data-ttu-id="09c0f-108">Beispiel 1: Löschen eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="09c0f-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="09c0f-109">Dieser Befehl löscht einen vorhandenen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="09c0f-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="09c0f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="09c0f-110">PARAMETERS</span></span>

### <span data-ttu-id="09c0f-111">-Context</span><span class="sxs-lookup"><span data-stu-id="09c0f-111">-Context</span></span>
<span data-ttu-id="09c0f-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="09c0f-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="09c0f-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="09c0f-113">This parameter is required.</span></span>

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

### <span data-ttu-id="09c0f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09c0f-114">-DefaultProfile</span></span>
<span data-ttu-id="09c0f-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="09c0f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="09c0f-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="09c0f-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="09c0f-117">Gibt an, ob Abonnements für das Produkt gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="09c0f-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="09c0f-118">Wenn dieser Parameter nicht angegeben ist und ein Abonnement vorhanden ist, löst dieses Cmdlet eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="09c0f-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="09c0f-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="09c0f-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="09c0f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09c0f-120">-PassThru</span></span>
<span data-ttu-id="09c0f-121">Gibt an, dass dieses Cmdlet einen Wert von $Ture zurückgibt, wenn dies erfolgreich ist, oder einen Wert von $false, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="09c0f-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="09c0f-122">-UserID</span><span class="sxs-lookup"><span data-stu-id="09c0f-122">-UserId</span></span>
<span data-ttu-id="09c0f-123">Gibt die ID des Benutzers an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="09c0f-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="09c0f-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="09c0f-124">-Confirm</span></span>
<span data-ttu-id="09c0f-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="09c0f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09c0f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09c0f-126">-WhatIf</span></span>
<span data-ttu-id="09c0f-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09c0f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09c0f-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="09c0f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09c0f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09c0f-129">CommonParameters</span></span>
<span data-ttu-id="09c0f-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09c0f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09c0f-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09c0f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09c0f-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09c0f-132">INPUTS</span></span>

### <span data-ttu-id="09c0f-133">Keine</span><span class="sxs-lookup"><span data-stu-id="09c0f-133">None</span></span>
<span data-ttu-id="09c0f-134">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="09c0f-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="09c0f-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09c0f-135">OUTPUTS</span></span>

### <span data-ttu-id="09c0f-136">Boolean</span><span class="sxs-lookup"><span data-stu-id="09c0f-136">Boolean</span></span>

## <span data-ttu-id="09c0f-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="09c0f-137">NOTES</span></span>

## <span data-ttu-id="09c0f-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09c0f-138">RELATED LINKS</span></span>

[<span data-ttu-id="09c0f-139">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="09c0f-139">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="09c0f-140">Neu – AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="09c0f-140">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="09c0f-141">Satz-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="09c0f-141">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


