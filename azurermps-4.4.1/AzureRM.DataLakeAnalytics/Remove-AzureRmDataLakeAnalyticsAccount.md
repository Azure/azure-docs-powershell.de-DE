---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 23f1ba9185b2a33c910afb0fc7ff0deb2a1cbf5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479277"
---
# <span data-ttu-id="f72a2-101">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f72a2-101">Remove-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="f72a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f72a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f72a2-103">Löscht ein Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="f72a2-103">Deletes a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f72a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f72a2-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f72a2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f72a2-105">DESCRIPTION</span></span>
<span data-ttu-id="f72a2-106">Mit dem Cmdlet **Remove-AzureRmDataLakeAnalyticsAccount** wird ein Azure Data Lake-Analyse Konto endgültig gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f72a2-106">The **Remove-AzureRmDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="f72a2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f72a2-107">EXAMPLES</span></span>

### <span data-ttu-id="f72a2-108">Beispiel 1: Entfernen eines Kontos</span><span class="sxs-lookup"><span data-stu-id="f72a2-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="f72a2-109">Mit diesem Befehl wird das angegebene Data Lake Analytics-Konto entfernt.</span><span class="sxs-lookup"><span data-stu-id="f72a2-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="f72a2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f72a2-110">PARAMETERS</span></span>

### <span data-ttu-id="f72a2-111">-Force</span><span class="sxs-lookup"><span data-stu-id="f72a2-111">-Force</span></span>
<span data-ttu-id="f72a2-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f72a2-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f72a2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f72a2-113">-Name</span></span>
<span data-ttu-id="f72a2-114">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="f72a2-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="f72a2-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f72a2-115">-PassThru</span></span>
<span data-ttu-id="f72a2-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f72a2-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f72a2-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="f72a2-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f72a2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f72a2-118">-ResourceGroupName</span></span>
<span data-ttu-id="f72a2-119">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="f72a2-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f72a2-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f72a2-120">-Confirm</span></span>
<span data-ttu-id="f72a2-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f72a2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f72a2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f72a2-122">-WhatIf</span></span>
<span data-ttu-id="f72a2-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f72a2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f72a2-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f72a2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f72a2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f72a2-125">-DefaultProfile</span></span>
<span data-ttu-id="f72a2-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f72a2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f72a2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f72a2-127">CommonParameters</span></span>
<span data-ttu-id="f72a2-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f72a2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f72a2-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f72a2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f72a2-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f72a2-130">INPUTS</span></span>

## <span data-ttu-id="f72a2-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f72a2-131">OUTPUTS</span></span>

### <span data-ttu-id="f72a2-132">bool</span><span class="sxs-lookup"><span data-stu-id="f72a2-132">bool</span></span>
<span data-ttu-id="f72a2-133">Wenn passthru angegeben ist, gibt true nach Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="f72a2-133">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="f72a2-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="f72a2-134">NOTES</span></span>

## <span data-ttu-id="f72a2-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f72a2-135">RELATED LINKS</span></span>

[<span data-ttu-id="f72a2-136">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f72a2-136">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f72a2-137">Neu – AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f72a2-137">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f72a2-138">Satz-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f72a2-138">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f72a2-139">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f72a2-139">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


