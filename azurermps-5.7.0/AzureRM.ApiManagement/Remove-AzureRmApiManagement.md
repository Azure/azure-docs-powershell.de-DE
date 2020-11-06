---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
ms.openlocfilehash: 197b1605d178c0aaa1c3f96580cb295306910232
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503906"
---
# <span data-ttu-id="46b4a-101">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="46b4a-101">Remove-AzureRmApiManagement</span></span>

## <span data-ttu-id="46b4a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46b4a-102">SYNOPSIS</span></span>
<span data-ttu-id="46b4a-103">Entfernt einen API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="46b4a-103">Removes an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46b4a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46b4a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46b4a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46b4a-105">DESCRIPTION</span></span>
<span data-ttu-id="46b4a-106">Mit dem Cmdlet **Remove-AzureRmApiManagement** wird ein Azure API-Verwaltungsdienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="46b4a-106">The **Remove-AzureRmApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="46b4a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46b4a-107">EXAMPLES</span></span>

### <span data-ttu-id="46b4a-108">Beispiel 1: Entfernen eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="46b4a-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="46b4a-109">Mit diesem Befehl wird der API-Verwaltungsdienst mit dem Namen ContosoApi entfernt.</span><span class="sxs-lookup"><span data-stu-id="46b4a-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="46b4a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="46b4a-110">PARAMETERS</span></span>

### <span data-ttu-id="46b4a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46b4a-111">-DefaultProfile</span></span>
<span data-ttu-id="46b4a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="46b4a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="46b4a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="46b4a-113">-Name</span></span>
<span data-ttu-id="46b4a-114">Gibt den Namen der API-Verwaltungs Bereitstellung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="46b4a-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="46b4a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46b4a-115">-PassThru</span></span>
<span data-ttu-id="46b4a-116">Gibt an, dass dieses Cmdlet den Wert $true zurückgibt, wenn der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="46b4a-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46b4a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46b4a-117">-ResourceGroupName</span></span>
<span data-ttu-id="46b4a-118">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltungs Bereitstellung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="46b4a-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="46b4a-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46b4a-119">-Confirm</span></span>
<span data-ttu-id="46b4a-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46b4a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46b4a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46b4a-121">-WhatIf</span></span>
<span data-ttu-id="46b4a-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46b4a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46b4a-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46b4a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46b4a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46b4a-124">CommonParameters</span></span>
<span data-ttu-id="46b4a-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46b4a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46b4a-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46b4a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46b4a-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46b4a-127">INPUTS</span></span>

### <span data-ttu-id="46b4a-128">Keine</span><span class="sxs-lookup"><span data-stu-id="46b4a-128">None</span></span>
<span data-ttu-id="46b4a-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="46b4a-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="46b4a-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46b4a-130">OUTPUTS</span></span>

### <span data-ttu-id="46b4a-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="46b4a-131">System.Boolean</span></span>

## <span data-ttu-id="46b4a-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="46b4a-132">NOTES</span></span>

## <span data-ttu-id="46b4a-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46b4a-133">RELATED LINKS</span></span>

[<span data-ttu-id="46b4a-134">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="46b4a-134">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="46b4a-135">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="46b4a-135">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="46b4a-136">Neu – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="46b4a-136">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="46b4a-137">Wiederherstellen – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="46b4a-137">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


