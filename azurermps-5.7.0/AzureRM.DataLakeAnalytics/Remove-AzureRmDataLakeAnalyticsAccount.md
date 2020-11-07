---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: f978925766fb664f5ddeaf3b6dffa94e55244f43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662581"
---
# <span data-ttu-id="26614-101">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="26614-101">Remove-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="26614-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="26614-102">SYNOPSIS</span></span>
<span data-ttu-id="26614-103">Löscht ein Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="26614-103">Deletes a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26614-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="26614-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26614-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26614-105">DESCRIPTION</span></span>
<span data-ttu-id="26614-106">Mit dem Cmdlet **Remove-AzureRmDataLakeAnalyticsAccount** wird ein Azure Data Lake-Analyse Konto endgültig gelöscht.</span><span class="sxs-lookup"><span data-stu-id="26614-106">The **Remove-AzureRmDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="26614-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26614-107">EXAMPLES</span></span>

### <span data-ttu-id="26614-108">Beispiel 1: Entfernen eines Kontos</span><span class="sxs-lookup"><span data-stu-id="26614-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="26614-109">Mit diesem Befehl wird das angegebene Data Lake Analytics-Konto entfernt.</span><span class="sxs-lookup"><span data-stu-id="26614-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="26614-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="26614-110">PARAMETERS</span></span>

### <span data-ttu-id="26614-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26614-111">-DefaultProfile</span></span>
<span data-ttu-id="26614-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="26614-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26614-113">-Force</span><span class="sxs-lookup"><span data-stu-id="26614-113">-Force</span></span>
<span data-ttu-id="26614-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="26614-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26614-115">-Name</span><span class="sxs-lookup"><span data-stu-id="26614-115">-Name</span></span>
<span data-ttu-id="26614-116">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="26614-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="26614-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26614-117">-PassThru</span></span>
<span data-ttu-id="26614-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="26614-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="26614-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="26614-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26614-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26614-120">-ResourceGroupName</span></span>
<span data-ttu-id="26614-121">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="26614-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26614-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="26614-122">-Confirm</span></span>
<span data-ttu-id="26614-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="26614-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26614-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26614-124">-WhatIf</span></span>
<span data-ttu-id="26614-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26614-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26614-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26614-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26614-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26614-127">CommonParameters</span></span>
<span data-ttu-id="26614-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26614-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26614-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26614-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26614-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="26614-130">INPUTS</span></span>

### <span data-ttu-id="26614-131">Keine</span><span class="sxs-lookup"><span data-stu-id="26614-131">None</span></span>
<span data-ttu-id="26614-132">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="26614-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="26614-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="26614-133">OUTPUTS</span></span>

### <span data-ttu-id="26614-134">bool</span><span class="sxs-lookup"><span data-stu-id="26614-134">bool</span></span>
<span data-ttu-id="26614-135">Wenn passthru angegeben ist, gibt true nach Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="26614-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="26614-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="26614-136">NOTES</span></span>

## <span data-ttu-id="26614-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="26614-137">RELATED LINKS</span></span>

[<span data-ttu-id="26614-138">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="26614-138">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="26614-139">Neu – AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="26614-139">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="26614-140">Satz-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="26614-140">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="26614-141">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="26614-141">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


