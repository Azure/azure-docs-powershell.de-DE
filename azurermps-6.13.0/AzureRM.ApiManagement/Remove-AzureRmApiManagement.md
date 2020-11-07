---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
ms.openlocfilehash: cee512445f457e7353d5766cd561788b00360b40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664129"
---
# <span data-ttu-id="90b7d-101">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="90b7d-101">Remove-AzureRmApiManagement</span></span>

## <span data-ttu-id="90b7d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="90b7d-103">Entfernt einen API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="90b7d-103">Removes an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90b7d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90b7d-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90b7d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90b7d-105">DESCRIPTION</span></span>
<span data-ttu-id="90b7d-106">Mit dem Cmdlet **Remove-AzureRmApiManagement** wird ein Azure API-Verwaltungsdienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="90b7d-106">The **Remove-AzureRmApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="90b7d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90b7d-107">EXAMPLES</span></span>

### <span data-ttu-id="90b7d-108">Beispiel 1: Entfernen eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="90b7d-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="90b7d-109">Mit diesem Befehl wird der API-Verwaltungsdienst mit dem Namen ContosoApi entfernt.</span><span class="sxs-lookup"><span data-stu-id="90b7d-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="90b7d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="90b7d-110">PARAMETERS</span></span>

### <span data-ttu-id="90b7d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90b7d-111">-DefaultProfile</span></span>
<span data-ttu-id="90b7d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="90b7d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90b7d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="90b7d-113">-Name</span></span>
<span data-ttu-id="90b7d-114">Gibt den Namen der API-Verwaltungs Bereitstellung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="90b7d-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="90b7d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90b7d-115">-PassThru</span></span>
<span data-ttu-id="90b7d-116">Gibt an, dass dieses Cmdlet den Wert $true zurückgibt, wenn der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="90b7d-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90b7d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90b7d-117">-ResourceGroupName</span></span>
<span data-ttu-id="90b7d-118">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltungs Bereitstellung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="90b7d-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="90b7d-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="90b7d-119">-Confirm</span></span>
<span data-ttu-id="90b7d-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90b7d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90b7d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90b7d-121">-WhatIf</span></span>
<span data-ttu-id="90b7d-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90b7d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90b7d-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90b7d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90b7d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90b7d-124">CommonParameters</span></span>
<span data-ttu-id="90b7d-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90b7d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90b7d-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90b7d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90b7d-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90b7d-127">INPUTS</span></span>

### <span data-ttu-id="90b7d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="90b7d-128">System.String</span></span>

## <span data-ttu-id="90b7d-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90b7d-129">OUTPUTS</span></span>

### <span data-ttu-id="90b7d-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="90b7d-130">System.Boolean</span></span>

## <span data-ttu-id="90b7d-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="90b7d-131">NOTES</span></span>

## <span data-ttu-id="90b7d-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90b7d-132">RELATED LINKS</span></span>

[<span data-ttu-id="90b7d-133">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="90b7d-133">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="90b7d-134">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="90b7d-134">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="90b7d-135">Neu – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="90b7d-135">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="90b7d-136">Wiederherstellen – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="90b7d-136">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


