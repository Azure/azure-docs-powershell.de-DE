---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
ms.openlocfilehash: 6d6c72702d03b3b2174c21c786fb373374cea739
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009385"
---
# <span data-ttu-id="ebf28-101">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ebf28-101">Set-AzBatchApplication</span></span>

## <span data-ttu-id="ebf28-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ebf28-102">SYNOPSIS</span></span>
<span data-ttu-id="ebf28-103">Aktualisiert die Einstellungen für die angegebene Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ebf28-103">Updates settings for the specified application.</span></span>

## <span data-ttu-id="ebf28-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebf28-104">SYNTAX</span></span>

```
Set-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebf28-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ebf28-105">DESCRIPTION</span></span>
<span data-ttu-id="ebf28-106">Das Cmdlet " **Satz-AzBatchApplication** " ändert die Einstellungen für die angegebene Azure-Batch Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ebf28-106">The **Set-AzBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="ebf28-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ebf28-107">EXAMPLES</span></span>

### <span data-ttu-id="ebf28-108">Beispiel 1: Aktualisieren einer Anwendung in einem Stapelverarbeitungs Konto</span><span class="sxs-lookup"><span data-stu-id="ebf28-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -AllowUpdates $False
```

<span data-ttu-id="ebf28-109">Mit diesem Befehl wird geändert, ob die Litware-Anwendung im ContosoBatch-Konto Updates zulässt.</span><span class="sxs-lookup"><span data-stu-id="ebf28-109">This command changes whether the Litware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="ebf28-110">Der Befehl ändert nicht die Standard Version oder den Anzeigenamen der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ebf28-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="ebf28-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebf28-111">PARAMETERS</span></span>

### <span data-ttu-id="ebf28-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="ebf28-112">-AccountName</span></span>
<span data-ttu-id="ebf28-113">Gibt den Namen des Batch Kontos an, für das dieses Cmdlet eine Anwendung ändert.</span><span class="sxs-lookup"><span data-stu-id="ebf28-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="ebf28-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="ebf28-114">-AllowUpdates</span></span>
<span data-ttu-id="ebf28-115">Gibt an, ob Pakete in der Anwendung mit der gleichen Versionszeichenfolge überschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="ebf28-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf28-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="ebf28-116">-ApplicationName</span></span>
<span data-ttu-id="ebf28-117">Gibt den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="ebf28-117">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf28-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebf28-118">-DefaultProfile</span></span>
<span data-ttu-id="ebf28-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ebf28-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebf28-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="ebf28-120">-DefaultVersion</span></span>
<span data-ttu-id="ebf28-121">Gibt an, welches Paket verwendet werden soll, wenn ein Client die Anwendung anfordert, aber keine Version angibt.</span><span class="sxs-lookup"><span data-stu-id="ebf28-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf28-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ebf28-122">-DisplayName</span></span>
<span data-ttu-id="ebf28-123">Gibt den Anzeigenamen für die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="ebf28-123">Specifies the display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf28-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebf28-124">-ResourceGroupName</span></span>
<span data-ttu-id="ebf28-125">Gibt den Namen der Ressourcengruppe an, die das Stapelverarbeitungs Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="ebf28-125">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf28-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebf28-126">CommonParameters</span></span>
<span data-ttu-id="ebf28-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebf28-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebf28-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebf28-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebf28-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ebf28-129">INPUTS</span></span>

### <span data-ttu-id="ebf28-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ebf28-130">System.String</span></span>

### <span data-ttu-id="ebf28-131">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ebf28-131">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ebf28-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ebf28-132">OUTPUTS</span></span>

### <span data-ttu-id="ebf28-133">System. void</span><span class="sxs-lookup"><span data-stu-id="ebf28-133">System.Void</span></span>

## <span data-ttu-id="ebf28-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="ebf28-134">NOTES</span></span>

## <span data-ttu-id="ebf28-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ebf28-135">RELATED LINKS</span></span>

[<span data-ttu-id="ebf28-136">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ebf28-136">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="ebf28-137">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ebf28-137">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="ebf28-138">Neu – AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ebf28-138">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="ebf28-139">Neu – AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ebf28-139">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="ebf28-140">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ebf28-140">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="ebf28-141">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ebf28-141">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)


