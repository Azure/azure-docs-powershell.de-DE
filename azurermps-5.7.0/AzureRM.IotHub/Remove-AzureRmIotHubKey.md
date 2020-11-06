---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
ms.openlocfilehash: 4f1c21f4f64193ec25a0392e094b8fd492ceba9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482905"
---
# <span data-ttu-id="70ab5-101">Remove-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="70ab5-101">Remove-AzureRmIotHubKey</span></span>

## <span data-ttu-id="70ab5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="70ab5-103">Entfernt einen IotHub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="70ab5-103">Removes an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70ab5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70ab5-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70ab5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70ab5-105">DESCRIPTION</span></span>
<span data-ttu-id="70ab5-106">Entfernt einen IotHub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="70ab5-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="70ab5-107">Wenn mehrere Schlüssel mit demselben Namen vorhanden sind, wird der erste in der Liste entfernt.</span><span class="sxs-lookup"><span data-stu-id="70ab5-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="70ab5-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70ab5-108">EXAMPLES</span></span>

### <span data-ttu-id="70ab5-109">Beispiel 1 Löschen eines IotHub</span><span class="sxs-lookup"><span data-stu-id="70ab5-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="70ab5-110">Entfernt den Schlüssel mit dem Namen iothubowner1 aus dem IotHub mit dem Namen "myiothub".</span><span class="sxs-lookup"><span data-stu-id="70ab5-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="70ab5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="70ab5-111">PARAMETERS</span></span>

### <span data-ttu-id="70ab5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70ab5-112">-DefaultProfile</span></span>
<span data-ttu-id="70ab5-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="70ab5-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70ab5-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="70ab5-114">-KeyName</span></span>
<span data-ttu-id="70ab5-115">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="70ab5-115">Name of the Key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70ab5-116">-Name</span><span class="sxs-lookup"><span data-stu-id="70ab5-116">-Name</span></span>
<span data-ttu-id="70ab5-117">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="70ab5-117">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70ab5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70ab5-118">-ResourceGroupName</span></span>
<span data-ttu-id="70ab5-119">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="70ab5-119">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70ab5-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="70ab5-120">-Confirm</span></span>
<span data-ttu-id="70ab5-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="70ab5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70ab5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70ab5-122">-WhatIf</span></span>
<span data-ttu-id="70ab5-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70ab5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70ab5-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70ab5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70ab5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70ab5-125">CommonParameters</span></span>
<span data-ttu-id="70ab5-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70ab5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70ab5-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70ab5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70ab5-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70ab5-128">INPUTS</span></span>

### <span data-ttu-id="70ab5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="70ab5-129">System.String</span></span>

## <span data-ttu-id="70ab5-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70ab5-130">OUTPUTS</span></span>

### <span data-ttu-id="70ab5-131">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="70ab5-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="70ab5-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="70ab5-132">NOTES</span></span>

## <span data-ttu-id="70ab5-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70ab5-133">RELATED LINKS</span></span>

