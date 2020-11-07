---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/set-azurermmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
ms.openlocfilehash: 2b0e8564f2a536c7b7eda5b9ae8ae3cc58bf41cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662843"
---
# <span data-ttu-id="b05d3-101">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="b05d3-101">Set-AzureRmMediaServiceKey</span></span>

## <span data-ttu-id="b05d3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b05d3-102">SYNOPSIS</span></span>
<span data-ttu-id="b05d3-103">Regeneriert einen Schlüssel, der für den Zugriff auf den dem Mediendienst zugeordneten Ruhe Endpunkt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b05d3-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b05d3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b05d3-104">SYNTAX</span></span>

```
Set-AzureRmMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b05d3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b05d3-105">DESCRIPTION</span></span>
<span data-ttu-id="b05d3-106">Das Cmdlet " **Satz-AzureRmMediaServiceKey** " generiert einen Schlüssel, der für den Zugriff auf den mit dem Mediendienst verknüpften Repräsentations Status Transfer (Ruhe)-Endpunkt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b05d3-106">The **Set-AzureRmMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="b05d3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b05d3-107">EXAMPLES</span></span>

### <span data-ttu-id="b05d3-108">Beispiel 1: Erneutes Generieren des Primärschlüssels für den Zugriff auf den Mediendienst</span><span class="sxs-lookup"><span data-stu-id="b05d3-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="b05d3-109">Mit diesem Befehl wird der Primärschlüssel für den Mediendienst mit dem Namen MediaService001, der zur Ressourcengruppe mit dem Namen ResourceGroup004 gehört, erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="b05d3-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="b05d3-110">Beispiel 2: Erneutes Generieren des sekundären Schlüssels, der für den Zugriff auf den Mediendienst verwendet wird</span><span class="sxs-lookup"><span data-stu-id="b05d3-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="b05d3-111">Mit diesem Befehl wird der sekundäre Schlüssel für den Mediendienst mit dem Namen MediaService002, der zur Ressourcengruppe mit dem Namen Resourcegroup123 gehört, erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="b05d3-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="b05d3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b05d3-112">PARAMETERS</span></span>

### <span data-ttu-id="b05d3-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="b05d3-113">-AccountName</span></span>
<span data-ttu-id="b05d3-114">Gibt den Namen des Medien Diensts an, der vom Cmdlet erneut generiert wird.</span><span class="sxs-lookup"><span data-stu-id="b05d3-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b05d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b05d3-115">-DefaultProfile</span></span>
<span data-ttu-id="b05d3-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b05d3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b05d3-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="b05d3-117">-KeyType</span></span>
<span data-ttu-id="b05d3-118">Gibt den Schlüsseltyp des Medien Diensts an.</span><span class="sxs-lookup"><span data-stu-id="b05d3-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="b05d3-119">Die zulässigen Werte für diesen Parameter sind: primär oder sekundär.</span><span class="sxs-lookup"><span data-stu-id="b05d3-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

```yaml
Type: KeyType
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b05d3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b05d3-120">-ResourceGroupName</span></span>
<span data-ttu-id="b05d3-121">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="b05d3-121">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="b05d3-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b05d3-122">-Confirm</span></span>
<span data-ttu-id="b05d3-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b05d3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b05d3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b05d3-124">-WhatIf</span></span>
<span data-ttu-id="b05d3-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b05d3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b05d3-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b05d3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b05d3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b05d3-127">CommonParameters</span></span>
<span data-ttu-id="b05d3-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b05d3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b05d3-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b05d3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b05d3-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b05d3-130">INPUTS</span></span>

### <span data-ttu-id="b05d3-131">Keine</span><span class="sxs-lookup"><span data-stu-id="b05d3-131">None</span></span>
<span data-ttu-id="b05d3-132">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="b05d3-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b05d3-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b05d3-133">OUTPUTS</span></span>

### <span data-ttu-id="b05d3-134">Microsoft. Azure. Commands. Media. Models. PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="b05d3-134">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="b05d3-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="b05d3-135">NOTES</span></span>

## <span data-ttu-id="b05d3-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b05d3-136">RELATED LINKS</span></span>

[<span data-ttu-id="b05d3-137">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="b05d3-137">Get-AzureRmMediaServiceKeys</span></span>](./Get-AzureRmMediaServiceKeys.md)


