---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: 16a60f5f9951aaa40ac8da8584e1c2690206cdb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504625"
---
# <span data-ttu-id="c4ecc-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c4ecc-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="c4ecc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4ecc-102">SYNOPSIS</span></span>
<span data-ttu-id="c4ecc-103">Ändert eine API-verwaltungsprotokollierung.</span><span class="sxs-lookup"><span data-stu-id="c4ecc-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4ecc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4ecc-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4ecc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4ecc-105">DESCRIPTION</span></span>
<span data-ttu-id="c4ecc-106">Das Cmdlet " **festlegen-AzureRmApiManagementLogger** " ändert die Einstellungen einer Azure API-Verwaltungs **Protokollierung**.</span><span class="sxs-lookup"><span data-stu-id="c4ecc-106">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="c4ecc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4ecc-107">EXAMPLES</span></span>

### <span data-ttu-id="c4ecc-108">Beispiel 1: Ändern einer Protokollierung</span><span class="sxs-lookup"><span data-stu-id="c4ecc-108">Example 1: Modify a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="c4ecc-109">Mit diesem Befehl wird eine Protokollierung geändert, die die ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="c4ecc-109">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="c4ecc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4ecc-110">PARAMETERS</span></span>

### <span data-ttu-id="c4ecc-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="c4ecc-111">-ConnectionString</span></span>
<span data-ttu-id="c4ecc-112">Gibt eine Azure Event Hubs-Verbindungszeichenfolge an, die Sende Richtlinienrechte umfasst.</span><span class="sxs-lookup"><span data-stu-id="c4ecc-112">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ecc-113">-Context</span><span class="sxs-lookup"><span data-stu-id="c4ecc-113">-Context</span></span>
<span data-ttu-id="c4ecc-114">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c4ecc-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c4ecc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4ecc-115">-DefaultProfile</span></span>
<span data-ttu-id="c4ecc-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4ecc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="c4ecc-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4ecc-117">-Description</span></span>
<span data-ttu-id="c4ecc-118">Gibt eine Beschreibung an.</span><span class="sxs-lookup"><span data-stu-id="c4ecc-118">Specifies a description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ecc-119">-Isgepuffert</span><span class="sxs-lookup"><span data-stu-id="c4ecc-119">-IsBuffered</span></span>
<span data-ttu-id="c4ecc-120">Gibt an, dass die Datensätze in der Protokollierung vor der Veröffentlichung gepuffert werden.</span><span class="sxs-lookup"><span data-stu-id="c4ecc-120">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="c4ecc-121">Wenn Datensätze gepuffert werden, werden Sie alle 15 Sekunden an Ereignis Hubs gesendet, oder wenn der Puffer 256 KB Nachrichten empfängt.</span><span class="sxs-lookup"><span data-stu-id="c4ecc-121">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="c4ecc-122">-Protokollierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="c4ecc-122">-LoggerId</span></span>
<span data-ttu-id="c4ecc-123">Gibt die ID der Protokollierung an, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4ecc-123">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="c4ecc-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c4ecc-124">-Name</span></span>
<span data-ttu-id="c4ecc-125">Gibt den Entitätsnamen eines Ereignis Hubs aus dem Azure Classic-Portal an.</span><span class="sxs-lookup"><span data-stu-id="c4ecc-125">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ecc-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4ecc-126">-PassThru</span></span>
<span data-ttu-id="c4ecc-127">Gibt an, dass dieses Cmdlet die  **PsApiManagementLogger** zurückgibt, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c4ecc-127">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c4ecc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4ecc-128">CommonParameters</span></span>
<span data-ttu-id="c4ecc-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4ecc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4ecc-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4ecc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4ecc-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4ecc-131">INPUTS</span></span>

### <span data-ttu-id="c4ecc-132">Keine</span><span class="sxs-lookup"><span data-stu-id="c4ecc-132">None</span></span>
<span data-ttu-id="c4ecc-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c4ecc-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c4ecc-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4ecc-134">OUTPUTS</span></span>

### <span data-ttu-id="c4ecc-135">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c4ecc-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="c4ecc-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4ecc-136">NOTES</span></span>

## <span data-ttu-id="c4ecc-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4ecc-137">RELATED LINKS</span></span>

[<span data-ttu-id="c4ecc-138">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c4ecc-138">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="c4ecc-139">Neu – AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c4ecc-139">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="c4ecc-140">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c4ecc-140">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


