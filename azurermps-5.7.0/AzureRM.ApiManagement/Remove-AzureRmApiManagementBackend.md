---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: 347a05c5e197a93458a64c4079ce1fd430e631f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496689"
---
# <span data-ttu-id="a217a-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a217a-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="a217a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a217a-102">SYNOPSIS</span></span>
<span data-ttu-id="a217a-103">Entfernt ein Back-End.</span><span class="sxs-lookup"><span data-stu-id="a217a-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a217a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a217a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a217a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a217a-105">DESCRIPTION</span></span>
<span data-ttu-id="a217a-106">Entfernt ein vom Bezeichner angegebenes Back-End aus der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="a217a-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="a217a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a217a-107">EXAMPLES</span></span>

### <span data-ttu-id="a217a-108">Beispiel 1: Entfernen des Back-End-123</span><span class="sxs-lookup"><span data-stu-id="a217a-108">Example 1: Remove the Backend 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="a217a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a217a-109">PARAMETERS</span></span>

### <span data-ttu-id="a217a-110">-Back-End-Nr</span><span class="sxs-lookup"><span data-stu-id="a217a-110">-BackendId</span></span>
<span data-ttu-id="a217a-111">Bezeichner des vorhandenen Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="a217a-111">Identifier of existing backend.</span></span>
<span data-ttu-id="a217a-112">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a217a-112">This parameter is required.</span></span>

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

### <span data-ttu-id="a217a-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a217a-113">-Context</span></span>
<span data-ttu-id="a217a-114">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a217a-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a217a-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a217a-115">This parameter is required.</span></span>

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

### <span data-ttu-id="a217a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a217a-116">-DefaultProfile</span></span>
<span data-ttu-id="a217a-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a217a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="a217a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a217a-118">-PassThru</span></span>
<span data-ttu-id="a217a-119">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a217a-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="a217a-120">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a217a-120">This parameter is optional.</span></span>
<span data-ttu-id="a217a-121">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="a217a-121">Default value is false.</span></span>

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

### <span data-ttu-id="a217a-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a217a-122">-Confirm</span></span>
<span data-ttu-id="a217a-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a217a-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a217a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a217a-124">-WhatIf</span></span>
<span data-ttu-id="a217a-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a217a-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a217a-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a217a-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a217a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a217a-127">CommonParameters</span></span>
<span data-ttu-id="a217a-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a217a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a217a-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a217a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a217a-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a217a-130">INPUTS</span></span>

### <span data-ttu-id="a217a-131">Keine</span><span class="sxs-lookup"><span data-stu-id="a217a-131">None</span></span>
<span data-ttu-id="a217a-132">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a217a-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a217a-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a217a-133">OUTPUTS</span></span>

### <span data-ttu-id="a217a-134">bool</span><span class="sxs-lookup"><span data-stu-id="a217a-134">bool</span></span>

## <span data-ttu-id="a217a-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="a217a-135">NOTES</span></span>

## <span data-ttu-id="a217a-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a217a-136">RELATED LINKS</span></span>

[<span data-ttu-id="a217a-137">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a217a-137">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="a217a-138">Neu – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a217a-138">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="a217a-139">Neu – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="a217a-139">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="a217a-140">Neu – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="a217a-140">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="a217a-141">Satz-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a217a-141">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
