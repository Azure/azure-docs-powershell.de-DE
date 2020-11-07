---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
ms.openlocfilehash: e9d117e9e81ee1189031b9e1f2f0a4094e9b9fcf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819051"
---
# <span data-ttu-id="3e2fb-101">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="3e2fb-101">Set-AzMediaServiceKey</span></span>

## <span data-ttu-id="3e2fb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3e2fb-102">SYNOPSIS</span></span>
<span data-ttu-id="3e2fb-103">Regeneriert einen Schlüssel, der für den Zugriff auf den dem Mediendienst zugeordneten Ruhe Endpunkt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3e2fb-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="3e2fb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e2fb-104">SYNTAX</span></span>

```
Set-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e2fb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e2fb-105">DESCRIPTION</span></span>
<span data-ttu-id="3e2fb-106">Das Cmdlet " **Satz-AzMediaServiceKey** " generiert einen Schlüssel, der für den Zugriff auf den mit dem Mediendienst verknüpften Repräsentations Status Transfer (Ruhe)-Endpunkt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3e2fb-106">The **Set-AzMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="3e2fb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e2fb-107">EXAMPLES</span></span>

### <span data-ttu-id="3e2fb-108">Beispiel 1: Erneutes Generieren des Primärschlüssels für den Zugriff auf den Mediendienst</span><span class="sxs-lookup"><span data-stu-id="3e2fb-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="3e2fb-109">Mit diesem Befehl wird der Primärschlüssel für den Mediendienst mit dem Namen MediaService001, der zur Ressourcengruppe mit dem Namen ResourceGroup004 gehört, erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="3e2fb-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="3e2fb-110">Beispiel 2: Erneutes Generieren des sekundären Schlüssels, der für den Zugriff auf den Mediendienst verwendet wird</span><span class="sxs-lookup"><span data-stu-id="3e2fb-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="3e2fb-111">Mit diesem Befehl wird der sekundäre Schlüssel für den Mediendienst mit dem Namen MediaService002, der zur Ressourcengruppe mit dem Namen Resourcegroup123 gehört, erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="3e2fb-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="3e2fb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e2fb-112">PARAMETERS</span></span>

### <span data-ttu-id="3e2fb-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="3e2fb-113">-AccountName</span></span>
<span data-ttu-id="3e2fb-114">Gibt den Namen des Medien Diensts an, der vom Cmdlet erneut generiert wird.</span><span class="sxs-lookup"><span data-stu-id="3e2fb-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e2fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e2fb-115">-DefaultProfile</span></span>
<span data-ttu-id="3e2fb-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3e2fb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2fb-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="3e2fb-117">-KeyType</span></span>
<span data-ttu-id="3e2fb-118">Gibt den Schlüsseltyp des Medien Diensts an.</span><span class="sxs-lookup"><span data-stu-id="3e2fb-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="3e2fb-119">Die zulässigen Werte für diesen Parameter sind: primär oder sekundär.</span><span class="sxs-lookup"><span data-stu-id="3e2fb-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

```yaml
Type: Microsoft.Azure.Management.Media.Models.KeyType
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2fb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e2fb-120">-ResourceGroupName</span></span>
<span data-ttu-id="3e2fb-121">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="3e2fb-121">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e2fb-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3e2fb-122">-Confirm</span></span>
<span data-ttu-id="3e2fb-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3e2fb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e2fb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e2fb-124">-WhatIf</span></span>
<span data-ttu-id="3e2fb-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3e2fb-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e2fb-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e2fb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e2fb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e2fb-127">CommonParameters</span></span>
<span data-ttu-id="3e2fb-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e2fb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e2fb-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e2fb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e2fb-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3e2fb-130">INPUTS</span></span>

### <span data-ttu-id="3e2fb-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3e2fb-131">System.String</span></span>

## <span data-ttu-id="3e2fb-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3e2fb-132">OUTPUTS</span></span>

### <span data-ttu-id="3e2fb-133">Microsoft. Azure. Commands. Media. Models. PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="3e2fb-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="3e2fb-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="3e2fb-134">NOTES</span></span>

## <span data-ttu-id="3e2fb-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3e2fb-135">RELATED LINKS</span></span>

[<span data-ttu-id="3e2fb-136">Get-AzMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="3e2fb-136">Get-AzMediaServiceKeys</span></span>](./Get-AzMediaServiceKeys.md)


