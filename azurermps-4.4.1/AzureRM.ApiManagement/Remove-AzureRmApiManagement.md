---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
ms.openlocfilehash: 5a46e75f7ce7b0639de015de975c321c9d5c1ed6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477441"
---
# <span data-ttu-id="3180a-101">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3180a-101">Remove-AzureRmApiManagement</span></span>

## <span data-ttu-id="3180a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3180a-102">SYNOPSIS</span></span>
<span data-ttu-id="3180a-103">Entfernt einen API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="3180a-103">Removes an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3180a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3180a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3180a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3180a-105">DESCRIPTION</span></span>
<span data-ttu-id="3180a-106">Mit dem Cmdlet **Remove-AzureRmApiManagement** wird ein Azure API-Verwaltungsdienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="3180a-106">The **Remove-AzureRmApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="3180a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3180a-107">EXAMPLES</span></span>

### <span data-ttu-id="3180a-108">Beispiel 1: Entfernen eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="3180a-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="3180a-109">Mit diesem Befehl wird der API-Verwaltungsdienst mit dem Namen ContosoApi entfernt.</span><span class="sxs-lookup"><span data-stu-id="3180a-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="3180a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3180a-110">PARAMETERS</span></span>

### <span data-ttu-id="3180a-111">-Name</span><span class="sxs-lookup"><span data-stu-id="3180a-111">-Name</span></span>
<span data-ttu-id="3180a-112">Gibt den Namen der API-Verwaltungs Bereitstellung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="3180a-112">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3180a-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3180a-113">-PassThru</span></span>
<span data-ttu-id="3180a-114">Gibt an, dass dieses Cmdlet den Wert $true zurückgibt, wenn der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="3180a-114">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="3180a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3180a-115">-ResourceGroupName</span></span>
<span data-ttu-id="3180a-116">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltungs Bereitstellung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3180a-116">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="3180a-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3180a-117">-Confirm</span></span>
<span data-ttu-id="3180a-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3180a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3180a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3180a-119">-WhatIf</span></span>
<span data-ttu-id="3180a-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3180a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3180a-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3180a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3180a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3180a-122">-DefaultProfile</span></span>
<span data-ttu-id="3180a-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3180a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3180a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3180a-124">CommonParameters</span></span>
<span data-ttu-id="3180a-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3180a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3180a-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3180a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3180a-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3180a-127">INPUTS</span></span>

## <span data-ttu-id="3180a-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3180a-128">OUTPUTS</span></span>

### <span data-ttu-id="3180a-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3180a-129">System.Boolean</span></span>

## <span data-ttu-id="3180a-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="3180a-130">NOTES</span></span>

## <span data-ttu-id="3180a-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3180a-131">RELATED LINKS</span></span>

[<span data-ttu-id="3180a-132">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3180a-132">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="3180a-133">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3180a-133">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="3180a-134">Neu – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3180a-134">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="3180a-135">Wiederherstellen – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3180a-135">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


