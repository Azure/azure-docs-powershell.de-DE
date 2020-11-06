---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
ms.openlocfilehash: a5919959f038b94a27f373124377466926494337
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503130"
---
# <span data-ttu-id="05bf5-101">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="05bf5-101">Remove-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="05bf5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="05bf5-103">Entfernt eine vorhandene API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="05bf5-103">Removes an existing API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05bf5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="05bf5-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05bf5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05bf5-105">DESCRIPTION</span></span>
<span data-ttu-id="05bf5-106">Das Cmdlet **Remove-AzureRmApiManagementGroup** entfernt eine vorhandene API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="05bf5-106">The **Remove-AzureRmApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="05bf5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05bf5-107">EXAMPLES</span></span>

### <span data-ttu-id="05bf5-108">Beispiel 1: Entfernen einer vorhandenen Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="05bf5-108">Example 1: Remove an existing management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="05bf5-109">Dieser Befehl entfernt eine vorhandene Verwaltungsgruppe mit dem Namen Group0001 und fordert den Benutzer nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="05bf5-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="05bf5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="05bf5-110">PARAMETERS</span></span>

### <span data-ttu-id="05bf5-111">-Context</span><span class="sxs-lookup"><span data-stu-id="05bf5-111">-Context</span></span>
<span data-ttu-id="05bf5-112">Gibt die Instanz eines **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="05bf5-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="05bf5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05bf5-113">-DefaultProfile</span></span>
<span data-ttu-id="05bf5-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="05bf5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="05bf5-115">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="05bf5-115">-GroupId</span></span>
<span data-ttu-id="05bf5-116">Gibt den Bezeichner einer Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="05bf5-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="05bf5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05bf5-117">-PassThru</span></span>
<span data-ttu-id="05bf5-118">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn es erfolgreich ist, oder einen Wert von $false, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="05bf5-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="05bf5-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="05bf5-119">-Confirm</span></span>
<span data-ttu-id="05bf5-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="05bf5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05bf5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05bf5-121">-WhatIf</span></span>
<span data-ttu-id="05bf5-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="05bf5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05bf5-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="05bf5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05bf5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05bf5-124">CommonParameters</span></span>
<span data-ttu-id="05bf5-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05bf5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05bf5-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05bf5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05bf5-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05bf5-127">INPUTS</span></span>

### <span data-ttu-id="05bf5-128">Keine</span><span class="sxs-lookup"><span data-stu-id="05bf5-128">None</span></span>
<span data-ttu-id="05bf5-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="05bf5-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="05bf5-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05bf5-130">OUTPUTS</span></span>

### <span data-ttu-id="05bf5-131">Boolean</span><span class="sxs-lookup"><span data-stu-id="05bf5-131">Boolean</span></span>

## <span data-ttu-id="05bf5-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="05bf5-132">NOTES</span></span>

## <span data-ttu-id="05bf5-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05bf5-133">RELATED LINKS</span></span>

[<span data-ttu-id="05bf5-134">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="05bf5-134">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="05bf5-135">Neu – AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="05bf5-135">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="05bf5-136">Satz-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="05bf5-136">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


